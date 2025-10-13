# BTN-Website

Biological Transport Networks research group website for the Center for Computational Biology at the Flatiron Institute.

## Structure

- `index.html` - Main website page
- `assets/css/ccb.css` - CCB color scheme stylesheet
- `assets/webfonts/` - Font Awesome icon fonts (minimal version)
- `images/` - Group images and visualizations
- `pdfs/` - Publication PDFs and posters

## Viewing the Website

To view the website locally:

```bash
python3 -m http.server 8080
```

Then open http://localhost:8080 in your browser.

## Customization

The website includes TODO comments in the HTML for sections that should be customized:
- Group logo/branding
- Team member information
- Real publications and links
- Actual software repositories
- News updates
- Contact information

## Color Scheme

The site uses the CCB (Center for Computational Biology) color palette with teal/cyan primary colors. To use a different center's colors, modify `assets/css/ccb.css` or create a new CSS file (e.g., cca.css, ccq.css) and update the link in index.html.