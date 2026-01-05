# Lore Playground Gallery v2 (Final Fix)

A minimalist image gallery displaying AI-generated artwork from the Promptofolio_Lore repository.

## Features

- Dense grid of thumbnails from GitHub branches
- Click-to-expand modal with high-resolution images
- Display of image metadata (prompt, negative prompt, seed, model, sampler, filter)
- One-click copy buttons for prompts and seeds
- Pink-gold metallic "LORE" logo with minimalist design
- Fully responsive design

## What's Fixed in v2 (Final Fix)

### Critical Bug Fixes (January 2024)

1. **Fixed incorrect metadata display**: The gallery now properly associates each image with its correct metadata from the CSV. When you click on SERONDA-PG-1, you now see the correct prompt "A centered portrait photograph..." instead of wrong data.

2. **Simplified and reliable URL construction**: Replaced the buggy GitHub API caching with direct URL construction based on known filename patterns:
   - SERONDA-PG-1 to 1010 → thumbnails1 branch, format: "Seronda-PG-X.jpg"
   - SERONDA-PG-1011 to 2044 → thumbnails2 branch, format: "SERONDA-PG-XXXX.jpg"
   - SERONDA-PG-2045 to 3018 → thumbnails3 branch, format: "SERONDA-PG-XXXX.jpg"
   - SERONDA-PG-3019+ → thumbnails4 branch, format: "SERONDA-PG-XXXX.jpg"

3. **Proper data mapping**: Created a `dataMap` that maps each File ID to its correct metadata, ensuring the click handler always shows the right information.

4. **Big images work correctly**: Images 2045 and 3019 now correctly show their Big3/Big4 versions in the modal.

### Added Debug Logging

Added console logs to help diagnose any remaining issues:
- Logs the gallery data structure
- Logs the data map for verification
- Logs which item was clicked and its data

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

## Image Source

Images are loaded from the GitHub repository:
- Repository: T0nt0o/Promptofolio_Lore
- Thumbnails from: thumbnails1, thumbnails2, thumbnails3, thumbnails4 branches
- High-resolution images from: Big3, Big4 branches

## Testing

Open the browser's developer console (F12) to see debug logs showing:
- The gallery data structure
- The data map for verification
- Which item was clicked and its correct metadata

## Browser Support

- Chrome/Edge (recommended)
- Firefox
- Safari
- Mobile browsers

## License

For personal use with proper attribution to the original artwork creators.
