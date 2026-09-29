# Dave project webmap

This repository contains a static web map that can be published with GitHub Pages.

## Live site

After pushing to GitHub, the site will be available at:

https://<your-github-username>.github.io/<your-repository-name>/

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

1. Push this folder to a new GitHub repository.
2. In GitHub, open Settings → Pages.
3. Set Source to "GitHub Actions".
4. The included workflow in `.github/workflows/pages.yml` will deploy the site automatically.

This setup keeps the map assets, CSV data, and annotation images in the repository so the relative paths continue to work on the hosted site.
