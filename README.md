# Cartman Royale portable export

Keep `../portable.html` and every `asset-part-*.js` file in this directory
together. Open `../portable.html` from a static web server or GitHub Pages.

The asset parts are loaded in numeric order. Each one appends base64 media
chunks to the shared `window.__portableAssetChunks` registry; the launcher
joins those chunks into the data URLs used by the existing game. The parts
are intentionally split below 22.5 MB so they stay under the 23 MB target.

Regenerate the export from the project root with:

```sh
node build-portable.js
```
