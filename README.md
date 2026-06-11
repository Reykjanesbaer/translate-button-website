# Google Translate Widget Demo

A small, static GitHub Pages demo of the Google Translate website widget. Each layout is loaded in its own HTML document and displayed on the main page in an iframe, preventing multiple widget initializations from interfering with one another.

## Widget types

The demo includes these three Google Translate widget layouts:

- **Vertical/default** (`vertical.html`)
- **Horizontal** (`horizontal.html`)
- **Simple** (`simple.html`)

`index.html` displays all three standalone widget pages.

## Allowed languages

Translation is limited to:

- English (`en`)
- Polish (`pl`)
- Spanish (`es`)
- Ukrainian (`uk`)
- Arabic (`ar`)

Every widget uses English as the page language and `en,pl,es,uk,ar` as its included languages.

## GitHub Pages setup

1. Push the repository to GitHub.
2. Open the repository's **Settings**.
3. Select **Pages** under **Code and automation**.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
5. Select the branch containing these files and choose the **`/ (root)`** folder.
6. Click **Save** and wait for GitHub Pages to publish the site.
7. Open the URL shown in the GitHub Pages settings.

No installation or build step is needed. The site uses only HTML, CSS, and JavaScript, with no npm packages, frameworks, build tools, or local dependencies.
