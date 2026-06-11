# Google Translate Widget Demo

This repository is a static GitHub Pages demo containing one default Google Translate website widget. The widget is embedded directly in `index.html`; it does not use iframes or alternate layouts.

## Languages

The page uses English as its source language and limits the visible selector to:

- English (`en`)
- Polish (`pl`)
- Spanish (`es`)
- Ukrainian (`uk`)
- Arabic (`ar`)

The widget configuration is:

```javascript
pageLanguage: 'en',
includedLanguages: 'en,pl,es,uk,ar'
```

## Run locally

No installation or build is required. Serve the repository root with any static file server, for example:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000/`.

Internet access is required for the selector because the Google Translate element script is loaded from `translate.google.com`.

## Publish with GitHub Pages

1. Open the repository on GitHub and select **Settings**.
2. Select **Pages** under **Code and automation**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the desired branch and the **`/ (root)`** folder.
5. Save the settings and open the published URL after deployment completes.

The project intentionally uses only HTML, CSS, and JavaScript. It has no framework, package manager, dependencies, or build tools.
