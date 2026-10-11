# Lord of Dice Documentation

Official documentation site for **Lord of Dice**, a mobile game by **High Tide Pacific**.

**Live site:** https://lopacn.github.io/lord-of-dice-docs/

## GitHub Pages Configuration

This site is served by GitHub Pages from the `main` branch root directory.

**To enable (if not already):**
1. Go to the repository **Settings** → **Pages**
2. Under **Source**, select **Deploy from a branch**
3. Choose branch **main** and folder **/ (root)**
4. Click **Save**

The `.nojekyll` file is present so GitHub serves files as-is without Jekyll processing.

## Site Structure

```
/
├── index.html           # Home page
├── privacy/
│   └── index.html       # Privacy Policy
├── assets/
│   └── style.css        # Shared stylesheet
├── 404.html             # Custom 404 page
├── .nojekyll            # Disable Jekyll
└── README.md            # This file
```

## Adding a New Documentation Page

1. **Create a directory** for the new page (e.g., `support/`, `terms/`, `faq/`)

2. **Create `index.html`** inside that directory using this template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>PAGE TITLE - Lord of Dice</title>
  <meta name="description" content="PAGE DESCRIPTION">
  <link rel="stylesheet" href="../assets/style.css">
</head>
<body>
  <header class="site-header">
    <h1><a href="../">Lord of Dice</a></h1>
  </header>
  <nav class="site-nav">
    <ul>
      <li><a href="../">Home</a></li>
      <li><a href="../privacy/">Privacy Policy</a></li>
      <!-- Add link to new page here in all nav sections -->
    </ul>
  </nav>
  <main class="content">
    <h1>PAGE TITLE</h1>
    <!-- Page content here -->
  </main>
  <footer class="site-footer">
    &copy; 2026 High Tide Pacific
  </footer>
</body>
</html>
```

3. **Update the navigation** in all existing pages:
   - `index.html`
   - `privacy/index.html`
   - `404.html`
   - Any other existing pages

   Add a link in the `<nav class="site-nav">` section:
   ```html
   <li><a href="NEW-SLUG/">Page Title</a></li>
   ```
   (Use `../NEW-SLUG/` from subpages)

4. **Add link on home page** in the `<ul class="doc-list">` section of `index.html`

5. **Commit and push** to `main`

## Notes

- All links are relative and work under the project-site base path
- No build step required—edit HTML files directly
- No JavaScript required to view the site
- No external scripts, trackers, or cookies
