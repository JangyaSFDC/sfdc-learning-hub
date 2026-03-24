# How to Publish New Articles on SFDC Learning Hub

## Quick Steps (3-minute process)

### Step 1: Copy the Template
1. Go to the `posts/` folder
2. Copy `template.html` and rename it (use dashes, no spaces):
   - Example: `soql-best-practices.html`, `lwc-lifecycle-hooks.html`

### Step 2: Edit the New File
Open your new file and update these 5 sections (marked with `STEP 1` through `STEP 5` in the comments):

| What to Change | Where |
|---|---|
| **Title & Description** | `<title>` and `<meta name="description">` in `<head>` |
| **Breadcrumb & Category** | The breadcrumb nav + category badge + date |
| **Article Content** | The `<section class="post-body">` area |
| **Tags** | The `<div class="post-tags">` section |
| **Related Posts** | Optional - update the 3 related articles |

### Step 3: Add to the Blog Page
Open `blog.html` and add a new `<article>` card at the top of the posts grid. Copy this template:

```html
<article class="post-card" data-category="apex">
    <div class="post-image">
        <div class="post-image-placeholder" style="--bg: linear-gradient(135deg, #1B96FF, #0D47A1);"><i class="fas fa-code"></i></div>
    </div>
    <div class="post-content">
        <div class="post-meta">
            <span class="post-category">Apex</span>
            <span class="post-date"><i class="far fa-calendar"></i> Mar 24, 2026</span>
        </div>
        <h3><a href="posts/YOUR-FILE-NAME.html">Your Post Title</a></h3>
        <p>Short description of the article (1-2 sentences).</p>
        <a href="posts/YOUR-FILE-NAME.html" class="read-more">Read More <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
```

### Step 4: Push to GitHub
Run these commands in the terminal:

```powershell
cd C:\Meher\malhotra\malhotra\website
git add -A
git commit -m "Published: Your article title"
git push
```

Your article will be live at: `https://jangyasfdc.github.io/sfdc-learning-hub/posts/YOUR-FILE-NAME.html`

---

## Category Colors & Icons Reference

| Category | Gradient Colors | Icon |
|---|---|---|
| **Apex** | `#1B96FF, #0D47A1` | `fa-code` |
| **LWC** | `#FF6B35, #E65100` | `fa-bolt` |
| **Admin** | `#2E844A, #1B5E20` | `fa-cogs` |
| **Integration** | `#9050E9, #6A1B9A` | `fa-plug` |
| **Flows** | `#DD7A01, #E65100` | `fa-project-diagram` |
| **Interview** | `#E3066A, #AD1457` | `fa-user-tie` |

## HTML Formatting Quick Reference

### Paragraph
```html
<p>Your text here.</p>
```

### Headings
```html
<h2>Main Section Heading</h2>
<h3>Sub Section Heading</h3>
```

### Code Block
```html
<pre><code>// Your code here
System.debug('Hello');</code></pre>
```

### Bullet List
```html
<ul>
    <li><strong>Item 1</strong> &mdash; Description</li>
    <li><strong>Item 2</strong> &mdash; Description</li>
</ul>
```

### Numbered List
```html
<ol>
    <li>First step</li>
    <li>Second step</li>
</ol>
```

### Callout / Quote
```html
<blockquote>
    <p>Important note or tip goes here.</p>
</blockquote>
```

### Bold & Inline Code
```html
<strong>bold text</strong>
<code>inline code</code>
```

### Special Characters in Code
Use these HTML entities inside code blocks:
- `<` → `&lt;`
- `>` → `&gt;`
- `&` → `&amp;`

---

## File Structure

```
website/
├── index.html          ← Homepage (add new post card here too)
├── blog.html           ← Blog listing (add card for every new post)
├── post.html           ← Original sample post
├── categories.html     ← Category pages
├── about.html          ← About page
├── css/styles.css      ← Styles (no changes needed)
├── js/main.js          ← JavaScript (no changes needed)
└── posts/              ← ALL NEW POSTS GO HERE
    ├── template.html   ← Copy this for each new post
    └── soql-best-practices.html  ← Example post
```
