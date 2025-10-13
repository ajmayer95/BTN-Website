# Quick Start Guide

## For First-Time Users

### Viewing the Website Locally

1. **Download/Clone this repository** to your computer

2. **Open a terminal/command prompt** and navigate to the website folder:
   ```bash
   cd path/to/BTN-Website
   ```

3. **Start a local web server** using one of these methods:
   
   **Option A - Python (easiest if you have Python):**
   ```bash
   python -m http.server 8000
   ```
   
   **Option B - Using your code editor:**
   - VS Code: Install "Live Server" extension, right-click `index.html`, select "Open with Live Server"
   - Other editors may have similar features

4. **Open your browser** and go to:
   - `http://localhost:8000` (for Python)
   - Or the URL shown in VS Code Live Server

5. **You should see the website!** Click through the navigation to explore all pages.

## Making Your First Edit

### Step 1: Edit the Group Name

1. Open `index.html` in a text editor
2. Find the line: `<h1 class="logo">BTN Research Group</h1>`
3. Change "BTN Research Group" to your actual group name
4. Save the file
5. Refresh your browser to see the change

### Step 2: Update the Home Page

1. Still in `index.html`, find the hero section
2. Update the welcome message and description
3. Save and refresh to see changes

### Step 3: Add Team Members

1. Open `members.html`
2. Find the Principal Investigator section
3. Replace `[Principal Investigator Name]` with the actual name
4. Update email, bio, and other information
5. Save and refresh

## Common Edits

### Changing Colors
- Open `css/style.css`
- Find `#3498db` (blue color) and replace with your preferred color
- Find `#2c3e50` (dark blue) and replace with your preferred color

### Adding a News Item
In `index.html`, add this in the news section:
```html
<article class="news-item">
    <span class="date">January 2024</span>
    <h4>Your News Title</h4>
    <p>Description of your news.</p>
</article>
```

### Adding a Publication
In `publications.html`, add:
```html
<article class="publication">
    <p class="authors">Author1, A., Author2, B.</p>
    <p class="title">"Your Paper Title"</p>
    <p class="venue"><em>Journal Name</em>, Vol(Issue), pages. (Year)</p>
    <p class="links">
        <a href="link-to-pdf" target="_blank">PDF</a> | 
        <a href="doi-link" target="_blank">DOI</a>
    </p>
</article>
```

## Publishing to GitHub Pages

Once you're happy with your changes:

1. Commit and push your changes to GitHub
2. Go to repository Settings → Pages
3. Select your branch (main) as the source
4. Save
5. Your website will be live at: `https://yourusername.github.io/repository-name/`

## Getting Help

- Full instructions: See main README.md
- HTML/CSS help: https://www.w3schools.com/
- GitHub Pages: https://pages.github.com/

## Checklist for Launch

- [ ] Updated group name everywhere
- [ ] Added all team members
- [ ] Updated research areas
- [ ] Added publications
- [ ] Updated contact information
- [ ] Tested all navigation links
- [ ] Checked on mobile device (resize browser)
- [ ] Ready to publish!