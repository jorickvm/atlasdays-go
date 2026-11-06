# go.atlasdays.app

Link host for "Open in AtlasDays" on [atlasdays.app](https://atlasdays.app). iOS opens an app from a universal link only when the link points to a different domain than the page it was tapped on, so these links live on their own subdomain.

- `.well-known/apple-app-site-association` lets AtlasDays open links under `/import/`.
- `import/index.html` is where a browser lands when the app is not installed: it forwards to `https://atlasdays.app/app/import/` with the URL fragment unchanged.
- `offers/home-screen.json` is read by the app's "Try Pro Free" Home Screen quick action: `code` is the offer code it pre-fills on the App Store redeem page, and `enabled: false` hides the action and sends taps to the normal paywall.
- Every other path redirects to atlasdays.app.

Published with GitHub Pages.
