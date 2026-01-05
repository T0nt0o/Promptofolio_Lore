# Lore Playground Gallery v2 (Fixed)

A minimalist image gallery displaying AI-generated artwork from the Promptofolio_Lore repository.

## Features

- Dense grid of thumbnails from GitHub branches
- Click-to-expand modal with high-resolution images
- Display of image metadata (prompt, negative prompt, seed, model, sampler, filter)
- One-click copy buttons for prompts and seeds
- Pink-gold metallic "LORE" logo with minimalist design
- Fully responsive design

## What's Fixed in v2 (Latest Update)

### Issues Resolved

1. **All images now load correctly**: Fixed the issue where only 3 images displayed while 4 were grayed out. The gallery now fetches ALL files from each GitHub branch and builds a complete asset map.

2. **Correct metadata matching**: Fixed the issue where clicking an image showed incorrect information. The gallery now properly maps each CSV entry to its corresponding image using normalized filenames.

3. **Big images now display**: Fixed the high-resolution image URLs. Images from SERONDA-PG-2045 onwards now correctly load their Big3/Big4 versions in the modal.

4. **Title field added**: Added the Title field display in the popup modal. If an image has a title (not "NA"), it now appears at the top of the info panel.

### Technical Improvements

- **Complete asset mapping**: Instead of caching one file per branch, the gallery now queries ALL files from thumbnails1-4 and Big3-4 branches
- **Normalized filename lookup**: Uses consistent filename normalization (uppercase, remove extension) for reliable matching
- **Dual lookup strategy**: First tries the GitHub API cache, then falls back to constructed URLs based on number ranges
- **Better error logging**: Added console logs to help diagnose any remaining issues

## Deployment

### Option 1: Netlify (Recommended)

1. Create a Netlify account at [netlify.com](https://netlify.com)
2. Drag and drop the `Lore-Gallery-v2` folder onto Netlify
3. Your site will be deployed instantly
4. Custom domain can be configured in Netlify settings

### Option 2: GitHub Pages

1. Create a new repository on GitHub
2. Upload the `Lore-Gallery-v2` folder contents
3. Go to repository Settings > Pages
4. Select the main branch as source
5. Your site will be available at `https://yourusername.github.io/repo-name/`

### Option 3: Any Web Host

Simply upload the entire `Lore-Gallery-v2` folder to your web server's public directory.

## Local Testing

To test locally, you need a local web server due to CORS restrictions:

### Using Python
```bash
cd Lore-Gallery-v2
python -m http.server 8000
```
Then open http://localhost:8000 in your browser

### Using Node.js
```bash
cd Lore-Gallery-v2
npx serve
```

## Image Source

Images are loaded from the GitHub repository:
- Repository: T0nt0o/Promptofolio_Lore
- Thumbnails from: thumbnails1, thumbnails2, thumbnails3, thumbnails4 branches
- High-resolution images from: Big3, Big4 branches

## Browser Support

- Chrome/Edge (recommended)
- Firefox
- Safari
- Mobile browsers

## License

For personal use with proper attribution to the original artwork creators.
