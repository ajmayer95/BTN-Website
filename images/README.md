# Images Directory

This directory is for storing images used on your website, including:

- Team member photos
- Research project images
- Lab photos
- Logo files
- Any other graphics

## Adding Images

### 1. Add Your Image Files

Place your image files in this directory. Supported formats:
- JPEG/JPG (recommended for photos)
- PNG (recommended for logos and graphics with transparency)
- GIF (for simple animations)
- SVG (for scalable vector graphics)

### 2. Naming Conventions

Use descriptive, lowercase names with hyphens:
- ✅ Good: `john-smith-headshot.jpg`, `lab-photo-2024.jpg`, `logo.png`
- ❌ Avoid: `IMG_1234.jpg`, `Photo 1.jpg`, `picture.jpg`

### 3. Using Images in HTML

To display an image on a web page, use the `<img>` tag:

```html
<img src="images/your-image.jpg" alt="Description of image">
```

**Important:** Always include the `alt` attribute for accessibility!

## Examples

### Team Member Photo

In `members.html`, replace the placeholder:

```html
<div class="member-photo">
    <img src="images/jane-doe.jpg" alt="Jane Doe">
    <div class="photo-placeholder">JD</div>
</div>
```

The placeholder text (JD) will show if the image doesn't load.

### Research Image

In `research.html`, add images to describe your research:

```html
<img src="images/research-setup.jpg" alt="Our lab setup for experiments">
```

### Logo

Replace "BTN Research Group" text with a logo in the header:

```html
<h1 class="logo">
    <img src="images/logo.png" alt="BTN Research Group" style="height: 40px;">
</h1>
```

## Image Optimization Tips

### Before Adding Images:

1. **Resize large images**
   - Headshots: 400x400 pixels is sufficient
   - Full-width images: 1200-1600 pixels wide
   - Don't upload 4000x3000 pixel images directly from a camera!

2. **Compress images**
   - Use tools like:
     - [TinyPNG](https://tinypng.com/) - Online compression
     - [ImageOptim](https://imageoptim.com/) - Mac app
     - [GIMP](https://www.gimp.org/) - Free image editor
   
3. **Choose the right format**
   - JPEG for photographs
   - PNG for logos, diagrams, or images with transparency
   - SVG for simple icons and logos that need to scale

### Why Optimize?

- Faster page loading
- Better user experience
- Less bandwidth usage
- Better mobile performance

## File Size Guidelines

- Headshots/portraits: < 100 KB
- Full-width photos: < 300 KB
- Background images: < 500 KB

## Example Directory Structure

```
images/
├── README.md (this file)
├── team/
│   ├── john-doe.jpg
│   ├── jane-smith.jpg
│   └── alex-johnson.jpg
├── research/
│   ├── lab-setup.jpg
│   ├── project-1-diagram.png
│   └── experiment-results.jpg
└── logo.png
```

You can organize images in subdirectories if you prefer!

## Need Help?

- [Web Image Basics](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML)
- [Image Optimization Guide](https://web.dev/fast/#optimize-your-images)
