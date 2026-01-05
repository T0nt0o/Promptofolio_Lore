# Lore Playground Gallery v2

A minimalist image gallery displaying AI-generated artwork from the Promptofolio_Lore repository.

## Features

- Dense grid of thumbnails from GitHub branches
- Click-to-expand modal with high-resolution images
- Display of image metadata (prompt, negative prompt, seed, model, sampler, filter)
- One-click copy buttons for prompts and seeds
- Pink-gold metallic "LORE" logo with minimalist design
- Fully responsive design

## What's New in v2

- **Fixed image loading issue**: Now uses GitHub API to fetch actual file URLs
- **More reliable image fetching**: Queries the GitHub API directly instead of constructing URLs
- **Better error handling**: Fallback URL construction if API fails
- **Improved caching**: Caches file URLs to minimize API calls

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
