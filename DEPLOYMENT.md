# Deploying to GitHub Pages

This guide will help you publish your website to GitHub Pages so it's accessible online.

## Prerequisites

- Your code is pushed to GitHub
- You have admin access to the repository

## Steps to Deploy

### 1. Enable GitHub Pages

1. Go to your repository on GitHub: `https://github.com/ajmayer95/BTN-Website`

2. Click on **Settings** (top right, near the repository name)

3. In the left sidebar, scroll down and click **Pages**

4. Under "Source":
   - Select the branch: **main** (or whichever branch has your website files)
   - Keep the folder as **/ (root)**
   - Click **Save**

5. Wait a few moments for GitHub to build your site

6. You'll see a message: "Your site is live at https://ajmayer95.github.io/BTN-Website/"

### 2. Visit Your Website

Your website will be available at:
```
https://ajmayer95.github.io/BTN-Website/
```

**Note:** It may take 2-10 minutes for the site to be available the first time.

### 3. Update Your Website

Any time you push changes to the main branch on GitHub, your website will automatically update within a few minutes.

Workflow:
1. Edit files locally
2. Preview with local server (`python -m http.server 8000`)
3. Commit changes (`git commit -m "Update content"`)
4. Push to GitHub (`git push`)
5. Wait a few minutes for GitHub Pages to rebuild
6. Refresh your live website to see changes

## Troubleshooting

### Site Not Showing

**Problem:** "404 - Page not found" when visiting the URL

**Solutions:**
- Wait 5-10 minutes after enabling GitHub Pages
- Check that `index.html` is in the root of your repository (not in a subfolder)
- Make sure the branch you selected in Settings → Pages is correct
- Try visiting `https://ajmayer95.github.io/BTN-Website/index.html` directly

### Changes Not Appearing

**Problem:** You pushed changes but the website still shows old content

**Solutions:**
- Wait 2-5 minutes for GitHub Pages to rebuild
- Hard refresh your browser (Ctrl+F5 on Windows, Cmd+Shift+R on Mac)
- Check that your changes were actually pushed to GitHub
- Go to the "Actions" tab in your repository to see if the deployment is in progress

### CSS/Styling Not Loading

**Problem:** Website shows unstyled HTML

**Solutions:**
- Check that `css/style.css` exists in your repository
- Verify the path in your HTML files is correct: `<link rel="stylesheet" href="css/style.css">`
- Make sure all files were committed and pushed

## Custom Domain (Optional)

If you want to use your own domain (e.g., `www.btn-research.org`) instead of the GitHub URL:

1. In Settings → Pages, scroll to "Custom domain"
2. Enter your domain name
3. Follow the instructions to configure your domain's DNS settings
4. Wait for DNS to propagate (can take up to 48 hours)

See [GitHub's custom domain documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site) for details.

## Need Help?

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Pages Troubleshooting](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-404-errors-for-github-pages-sites)
