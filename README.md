# QxFlow website

A static, single-page site built for GitHub Pages. No build step.

## Put it online

1. Upload everything in this folder to the root of your `<name>.github.io` repository (keep the `assets/` folder and the `.nojekyll` file).
2. In the repository, open **Settings > Pages** and set the source to the `main` branch, root folder.
3. The site appears at `https://<name>.github.io/` a minute or two later.

## Before you publish

Open `index.html`, scroll to the script at the bottom and set your address:

```js
var CONTACT_EMAIL = 'YOUR-EMAIL@example.com';
```

Every "Book a demo" button uses it.

The link-preview image (`og:image`, near the top of `index.html`) currently points at `https://ggggggyyyyyy.github.io/qxflow/assets/og.jpg`. Change it, and `og:url`, if the site moves to its own domain.

## Add or change a case demo

1. Put the clip and its poster image in `assets/`, for example `case-sensitivity.mp4` and `case-sensitivity.jpg`.
2. Add one entry to the `CASES` list in the same script:

```js
{ n: '05', role: 'prep', roleName: 'Preparer', secs: 12,
  title: 'Short title of the case',
  text: 'One or two sentences on what the agent does.',
  src: 'assets/case-sensitivity.mp4', poster: 'assets/case-sensitivity.jpg' }
```

`role` sets the tag colour: `prep` (teal), `rev` (blue) or `appr` (amber).

Clip guidelines: 5 to 20 seconds, 1280x720, H.264 `.mp4`, no audio, about 2 MB or less. Clips play muted and advance to the next case when they end.

## Files

- `index.html`: the page, its styles and its script
- `assets/hero-reel.mp4`: the short reel under the headline
- `assets/case-*.mp4` and `.jpg`: the four case clips and their posters
- `assets/favicon.svg`, `assets/og.jpg`: browser icon and link-preview image
- `.nojekyll`: tells GitHub Pages to serve the files as they are

Fonts load from Google Fonts (Inter, Inter Tight, JetBrains Mono, STIX Two Text).
