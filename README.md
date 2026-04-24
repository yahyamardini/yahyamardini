# Personal Website

This repository contains a static personal website built with plain HTML5 and a
single CSS file. It is intended to be served directly from the repository root
with GitHub Pages.

## Run locally

From the repository root:

```bash
python3 -m http.server
```

Then open `http://localhost:8000` in a browser.

## Deploy with GitHub Pages

1. Push the repository to the `main` branch on GitHub.
2. In the repository settings, open **Pages**.
3. Set the source to deploy from the `main` branch and the repository root.
4. Save the settings and wait for GitHub Pages to publish the site.

All internal links are relative so the site works when served from the repo
root without a build step.