# Google Translate Widget Demos

This repository is a static GitHub Pages demo of four isolated Google Translate controls:

- Vertical/default Google Translate widget
- Horizontal Google Translate widget
- Simple Google Translate widget
- Payload-style custom `IS` translate button

The landing page embeds each demo in a separate iframe. Keeping each Google Translate instance in its own standalone document avoids conflicts that can occur when several widgets initialize in one page.

## Pages

- `index.html` — GitHub Pages landing page containing all four demo cards
- `vertical.html` — vertical/default widget
- `horizontal.html` — horizontal inline widget
- `simple.html` — simple inline widget
- `payload-style.html` — custom `IS` button backed by the simple Google Translate widget

## Languages

Every widget uses English as its source language and limits its selector to:

- English (`en`)
- Polish (`pl`)
- Spanish (`es`)
- Ukrainian (`uk`)
- Arabic (`ar`)

The shared configuration is:

```javascript
pageLanguage: 'en',
includedLanguages: 'en,pl,es,uk,ar'
```

## Run locally

The demo uses only static HTML, CSS, and vanilla JavaScript. It has no package manager, framework, dependencies, or build step. Serve the repository root with a static file server:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000/`.

Internet access is required because Google's external Translate script controls the final rendered widget appearance and behavior.

## GitHub Pages

Publish the repository root from the desired branch using **Settings → Pages → Deploy from a branch**. No build configuration is needed.

## Payload-style prototype

`payload-style.html` is a visual and technical prototype for a custom `IS` language button. It keeps a Google Translate simple-layout widget underneath the custom control, but it is not the final Payload CMS implementation.
