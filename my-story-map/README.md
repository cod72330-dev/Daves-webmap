double-click `index.html` — you'll see a warning banner in that case. To test
# Sampled Locations Map

A Leaflet map that plots the coordinates encoded in PNG filenames, displays
each image in a marker popup, and lists locations in a fly-to sidebar.

## Files

- `index.html` redirects the published site to the map.
- `my-story-map/index.html` contains the map application.
- `annotation_png/` contains the annotation images and `manifest.json`.
- `.venv/` is local-only and excluded from Git.

The manifest is used instead of a directory listing because static hosts such
as GitHub Pages do not generate browsable file listings. If images are added
or removed, regenerate `annotation_png/manifest.json` from the PNG filenames.

## Run locally

Start a server from the repository root:

```powershell
python -m http.server 8000
```

Open `http://localhost:8000/` in a browser.

## Publish with GitHub Pages

Upload the entire repository root, including `annotation_png/` and
`my-story-map/`. In GitHub, open **Settings → Pages**, select **Deploy from a
branch**, choose the `main` branch and `/(root)`, then save. The root
`index.html` forwards visitors to the map.

The annotation images total about 586 MB, so the repository and initial upload
are large. Keep the images and manifest together at the repository root so the
map's relative URLs continue to work.
