# go.atlasdays.app

Link host for "Open in AtlasDays" on [atlasdays.app](https://atlasdays.app). iOS opens an app from a universal link only when the link points to a different domain than the page it was tapped on, so these links live on their own subdomain.

- `.well-known/apple-app-site-association` lets AtlasDays open links under `/import/`.
- `import/index.html` is where a browser lands when the app is not installed: it forwards to `https://atlasdays.app/app/import/` with the URL fragment unchanged.
- Every other path redirects to atlasdays.app.

Published with GitHub Pages.
