# Dave project webmap

This repository is configured for a single static GitHub Pages deployment.

## Live site

Once the repository is pushed and GitHub Pages is enabled, the site will be available at:

https://<your-github-username>.github.io/Daves-webmap/

The root page redirects visitors to the story map in the `my-story-map/` folder.

## Local preview

From the repository root:

```bash
python -m http.server 8000
```

Then open:

- http://localhost:8000/
- http://localhost:8000/my-story-map/

## Publish to GitHub Pages

1. Push this repository to GitHub.
2. In GitHub, open Settings → Pages.
3. Set Source to "GitHub Actions".
4. The workflow in `.github/workflows/pages.yml` will deploy the site automatically.

This setup keeps one clean static site with the map assets, CSV data, and annotation images in the same repository so the relative links keep working on the live site.
