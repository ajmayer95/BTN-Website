# BTN Research Group Website

A basic, editable website template for the BTN Research Group. This website is designed to be easy to edit by all group members and can be previewed locally before deployment.

## 📁 Project Structure

```
BTN-Website/
├── index.html          # Home page
├── members.html        # Team members page
├── research.html       # Research areas and projects
├── publications.html   # Publications list
├── contact.html        # Contact information
├── css/
│   └── style.css      # Stylesheet for all pages
├── images/            # Directory for photos and images (create as needed)
└── README.md          # This file
```

## 🚀 Quick Start - View Locally

There are several ways to preview the website locally on your computer:

### Method 1: Using Python (Recommended)

If you have Python installed:

```bash
# Navigate to the project directory
cd BTN-Website

# Python 3
python -m http.server 8000

# Python 2 (if Python 3 is not available)
python -m SimpleHTTPServer 8000
```

Then open your browser and visit: `http://localhost:8000`

### Method 2: Using Node.js

If you have Node.js installed, you can use `http-server`:

```bash
# Install http-server globally (one time only)
npm install -g http-server

# Run the server
http-server
```

Then open your browser and visit: `http://localhost:8080`

### Method 3: Using VS Code Live Server

1. Install the "Live Server" extension in VS Code
2. Right-click on `index.html`
3. Select "Open with Live Server"
4. The website will automatically open in your browser

### Method 4: Direct File Opening (Limited)

You can simply double-click `index.html` to open it in your browser. However, this method may have limitations with certain features.

## ✏️ Editing the Website

### Basic Content Editing

All website content is in HTML files. You can edit them with any text editor:

1. **Text Content**: Look for text between HTML tags and replace with your content
   ```html
   <h2>Welcome to BTN Research Group</h2>  <!-- Change this text -->
   <p>Your description here</p>             <!-- Change this text -->
   ```

2. **Links**: Update `href` attributes
   ```html
   <a href="mailto:your-email@institution.edu">your-email@institution.edu</a>
   ```

3. **Images**: Add your images to the `images/` folder (create it if needed)
   ```html
   <img src="images/yourphoto.jpg" alt="Description">
   ```

### Key Sections to Edit

#### 1. Home Page (`index.html`)
- Update the hero section with your group name and tagline
- Edit the "About Our Group" section
- Update research highlights
- Add latest news and announcements

#### 2. Members Page (`members.html`)
- Add your Principal Investigator information
- List postdocs, graduate students, and undergraduates
- Update alumni section
- Add photos to `images/` folder and link them

#### 3. Research Page (`research.html`)
- Describe your research areas
- List current projects
- Update collaborations
- Add funding sources

#### 4. Publications Page (`publications.html`)
- Add your publications organized by year
- Include links to PDFs, DOIs, and code repositories
- Update profile links (Google Scholar, ORCID, etc.)

#### 5. Contact Page (`contact.html`)
- Update address and contact information
- Add office hours
- Include information about joining the group
- Optional: Embed a map

### Styling Changes

All visual styling is in `css/style.css`. You can customize:

- **Colors**: Search for color codes (e.g., `#3498db`) and replace them
- **Fonts**: Change the `font-family` property
- **Spacing**: Adjust `padding` and `margin` values
- **Layout**: Modify grid and flexbox properties

## 🎨 Adding Images

1. Create an `images` directory if it doesn't exist:
   ```bash
   mkdir images
   ```

2. Add your images to this directory (JPEG, PNG, etc.)

3. Reference them in HTML:
   ```html
   <img src="images/team-photo.jpg" alt="Team Photo">
   ```

## 📝 Tips for Group Members

1. **Test locally first**: Always preview changes locally before publishing
2. **Use descriptive file names**: Name images clearly (e.g., `john-doe-headshot.jpg`)
3. **Keep backups**: Save copies before making major changes
4. **Be consistent**: Follow the existing format when adding new content
5. **Check all pages**: Make sure navigation works across all pages
6. **Optimize images**: Compress large images before adding them

## 🌐 Publishing the Website

Once you're happy with the local preview, you can publish the website using:

### GitHub Pages (Free and Easy)

1. Go to your repository settings on GitHub
2. Navigate to "Pages" section
3. Under "Source", select the branch (usually `main`)
4. Click "Save"
5. Your website will be available at: `https://ajmayer95.github.io/BTN-Website/`

### Other Hosting Options

- **Netlify**: Drag and drop deployment
- **Vercel**: Git-based deployment
- **Traditional Web Hosting**: Upload via FTP to your institution's server

## 🔧 Troubleshooting

**Problem**: Website doesn't look right when opened directly
- **Solution**: Use one of the local server methods above

**Problem**: Images not showing
- **Solution**: Check that image paths are correct and files exist

**Problem**: Navigation broken
- **Solution**: Ensure all HTML files are in the root directory

**Problem**: CSS not loading
- **Solution**: Verify the `css/style.css` file exists and the path is correct

## 🤝 Contributing

All group members can contribute! To make changes:

1. Clone or download the repository
2. Make your edits to the HTML/CSS files
3. Preview locally to test
4. Commit and push your changes
5. The website will update automatically (if using GitHub Pages)

## 📞 Need Help?

If you're having trouble editing the website:
1. Check this README for common solutions
2. Ask a group member who has edited it before
3. Refer to basic HTML/CSS tutorials online:
   - [HTML Basics](https://developer.mozilla.org/en-US/docs/Learn/HTML)
   - [CSS Basics](https://developer.mozilla.org/en-US/docs/Learn/CSS)

## 📄 License

This template is free to use and modify for your research group.