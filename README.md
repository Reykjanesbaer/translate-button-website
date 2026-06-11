# Google Translate Widget Demos

This repository is a static GitHub Pages demo of six isolated Google Translate controls — three standard widget layouts and three custom Payload-style `IS` button variants:

1. Vertical/default Google Translate widget
2. Horizontal Google Translate widget
3. Simple Google Translate widget
4. Payload-style custom `IS` button using the SIMPLE layout
5. Payload-style custom `IS` button using the standard/default selector
6. Payload-style custom `IS` button using the horizontal inline layout

The landing page embeds each demo in a separate iframe. Keeping each Google Translate instance in its own standalone document avoids conflicts that can occur when several widgets initialize in one page.

## Pages

- `index.html` — GitHub Pages landing page containing all six demo cards
- `vertical.html` — vertical/default widget
- `horizontal.html` — horizontal inline widget
- `simple.html` — simple inline widget
- `payload-style.html` — custom `IS` button backed by the SIMPLE Google Translate layout
- `payload-style-default.html` — custom `IS` button backed by the standard/default selector
- `payload-style-horizontal.html` — custom `IS` button backed by the horizontal inline layout

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

## Payload-style prototypes

The three `payload-style*.html` pages are visual and technical prototypes for a custom `IS` language button modelled on the Reykjanesbær Payload/Vercel header control. Each keeps a Google Translate widget hidden underneath the custom control and differs only in the underlying Google layout it initializes:

- `payload-style.html` — SIMPLE layout; the button forwards clicks to Google's language menu.
- `payload-style-default.html` — standard/default selector; the real `<select>` is overlaid invisibly so the button opens the native dropdown.
- `payload-style-horizontal.html` — horizontal inline layout; same invisible `<select>` overlay behavior.

The visible `IS` button looks identical across all three; they are prototypes, not the final Payload CMS implementation.
