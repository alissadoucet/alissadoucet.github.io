# Alissa's Website — Quick Reference Guide

## Your site address
https://alissadoucet.github.io

## File structure
```
alissadoucet.github.io/
├── index.html              ← your main site (all sections)
├── assets/
│   └── Doucet_CV.pdf       ← your CV (replace to update)
├── images/                  ← all your photos go here
│   ├── portrait.jpg
│   ├── strip-1.jpg
│   ├── strip-2.jpg
│   ├── strip-3.jpg
│   ├── strip-4.jpg
│   ├── research-macro.jpg
│   ├── research-monitoring.jpg
│   ├── research-community.jpg
│   ├── research-rapid.jpg
│   ├── contact-photo.jpg
│   ├── gallery-1.jpg ... gallery-6.jpg
│   └── (any post images)
└── posts/
    ├── post-template.html   ← copy this for each new post
    └── (your posts here)
```

## How to add photos

1. Crop your photos to square (1:1 ratio) — 800×800px is ideal
2. Upload them to the `images/` folder on GitHub
3. Edit `index.html` and find the placeholder you want to replace
4. Delete the `<div class="placeholder-label">...</div>` block
5. Add: `<img src="images/your-filename.jpg" alt="Description">`
6. Commit changes

### Example — replacing the portrait:

BEFORE:
```html
<div class="hero-portrait fade-in">
  <div class="placeholder-label">
    <svg>...</svg>
    Portrait
  </div>
</div>
```

AFTER:
```html
<div class="hero-portrait fade-in">
  <img src="images/portrait.jpg" alt="Alissa Marie Doucet">
</div>
```

## How to write a blog post

1. On GitHub, go to the `posts/` folder
2. Open `post-template.html` and click the copy/raw button
3. Click "Add file" → "Create new file"
4. Name it something short and descriptive: `warren-woods-june-2026.html`
5. Paste the template content
6. Edit these parts:
   - The `<title>` tag in the head
   - The `<meta name="description">` tag
   - The hero image `src` (or delete the hero div if no image)
   - The date and title in the post header
   - The body content — write in plain paragraphs using `<p>` tags
7. Commit the new file

### Then link it from the main page:

8. Edit `index.html`
9. Find one of the blog cards in the Reflections section
10. Change the `href="#"` to `href="posts/your-filename.html"`
11. Update the date and title text
12. Optionally add a photo to the card
13. Commit changes

### Quick HTML reference for writing posts:

```html
<p>A regular paragraph.</p>

<p>Text with <strong>bold</strong> and <em>italic</em> words.</p>

<p>A <a href="https://example.com">link to somewhere</a>.</p>

<h2>Big Section Heading</h2>

<h3>Smaller Sub-Heading</h3>

<img src="../images/my-photo.jpg" alt="Description of image">
<p class="caption">Photo caption here.</p>

<blockquote>A quote or field journal excerpt.</blockquote>

<ul>
  <li>Bullet point one</li>
  <li>Bullet point two</li>
</ul>
```

## How to update your CV

1. Go to `assets/` folder on GitHub
2. Delete the old `Doucet_CV.pdf`
3. Upload the new one with the same filename
4. Commit — the link on your site updates automatically

## How to add more gallery photos

1. Upload new images to `images/`
2. Edit `index.html`, find the gallery grid
3. Add a new block:
```html
<div class="gallery-item">
  <img src="images/gallery-new.jpg" alt="Description">
</div>
```
4. Commit changes

## How to add a new blog card on the main page

Find the `blog-grid` div in `index.html` and add:
```html
<a href="posts/your-post.html" class="blog-card">
  <div class="blog-card-photo">
    <img src="images/post-photo.jpg" alt="Post description">
  </div>
  <div class="blog-card-body">
    <div class="blog-card-date">Month Day, Year</div>
    <h3>Your Post Title</h3>
  </div>
</a>
```

## Tips
- Always write `alt="..."` descriptions for photos (accessibility + SEO)
- Keep image file sizes under 500KB for fast loading (use squoosh.app to compress)
- Test your changes by visiting your site after committing — takes ~1 minute to update
- If something breaks, GitHub keeps history — you can always revert to a previous version
