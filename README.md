# Division 2 Agent Build Tracker v0.1

A static, local-first mobile web app. No backend or Ubisoft API required.

## Run locally

From the folder containing `index.html`, run `python3 -m http.server 8000` and visit `http://localhost:8000` on the same computer. For iPhone installation, deploy to an HTTPS host.

## Deploy with GitHub Pages

1. Create a public GitHub repository.
2. Upload all five files in this folder to the repository root.
3. In Settings > Pages, select **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Visit the HTTPS Pages URL after deployment.
5. In iPhone Safari, use Share > Add to Home Screen.

## Screenshot OCR

Choose an image, tap **Scan screenshot**, inspect the text, and tap **Copy OCR into notes**. Manually transfer verified item data to the correct slots. OCR uses Tesseract.js v5 from jsDelivr and may download language/model files; first use requires internet. The image is processed in-browser, not uploaded to an app backend. The CDN is a third party; use a self-hosted OCR bundle if offline independence is required.

## Data

Builds live in browser localStorage, not synced between devices. Use Export backup regularly. Import backup merges by build ID. Clearing Safari website data or changing site origin may erase local data. The app does not automatically parse item attributes or screenshots into fields yet.

## Caveats

This is an MVP. OCR accuracy varies. The web app icon is SVG (some iOS versions may prefer PNG). The service worker caches the application shell, not the external OCR library. No stat calculator, automatic equipment detection, cloud sync, or authentication yet.
