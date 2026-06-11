# Google Translate Widget Layout Demo

This repository is a static GitHub Pages demo showing three Google Translate website widget layouts together on one page:

- Vertical/default
- Horizontal
- Simple

All three widgets are embedded directly in `index.html` and initialized by one callback. The project uses only HTML, CSS, and vanilla JavaScript—there is no framework, package manager, dependency installation, or build step.

## Languages

The page uses English as its source language and limits each widget's language selector to:

- English (`en`)
- Polish (`pl`)
- Spanish (`es`)
- Ukrainian (`uk`)
- Arabic (`ar`)

Each widget uses the same language configuration:

```javascript
pageLanguage: 'en',
includedLanguages: 'en,pl,es,uk,ar'
```

The three widgets use Google's `VERTICAL`, `HORIZONTAL`, and `SIMPLE` inline layout constants and render in separate containers on the same page.

## Run locally

No installation or build is required. You can open `index.html` directly, or serve the repository root with a static file server:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000/`.

Internet access is required for the widgets because the Google Translate element script is loaded from `translate.google.com`. Google may also inject additional iframes, controls, or translation banners when the widget is used.

## Publish with GitHub Pages

1. Open the repository on GitHub and select **Settings**.
2. Select **Pages** under **Code and automation**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the desired branch and the **`/ (root)`** folder.
5. Save the settings and open the published URL after deployment completes.
