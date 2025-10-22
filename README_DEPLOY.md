
# Deployable Map Site (Netlify / GitHub Pages)

This folder is ready to upload as-is.

## Files
- `index.html` — the site entry with your custom-image Leaflet map
- `assets/world-custom.png` — your map background
- `assets/members_xy.json` — your data points (X/Y pixels)
- `_redirects` — (Netlify) SPA fallback; harmless on GitHub Pages

## Deploy to Netlify (drag & drop)
1. Go to https://app.netlify.com/drop
2. Drag the entire *deployable-map-site* folder onto the page.
3. Netlify will give you a public URL like `https://your-site-name.netlify.app/`

## Deploy to GitHub Pages
1. Create a new repo and commit the contents of this folder.
2. In repo Settings → Pages → Source: `Deploy from a branch`, Branch: `main`, Folder: `/ (root)`.
3. Wait for the Page to build. Your site will be `https://<user>.github.io/<repo>/`

## Using in Wix
- In Wix Editor: Add → Embed → Custom Embeds → Embed a Widget (Website Address)
- Paste your public URL (Netlify or GitHub Pages)
- Resize the frame (full width, ~70vh tall)

## Updating Points
Edit `assets/members_xy.json` and re-deploy. Each item is:
{
  "name": "Your Place",
  "x": 1234,
  "y": 567,
  "url": "https://example.com/your-place"
}

Tip: Measure x/y in your graphics tool by hovering over the desired point on the image.

## Notes
- No external map tiles; everything is your image + Leaflet.
- Wheel zoom is disabled for friendlier page scroll; enable in `index.html` if desired.
