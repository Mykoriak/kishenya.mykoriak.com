# kishenya.mykoriak.com

Landing, help and privacy pages for the Kishenya iPhone app (repo `Mykoriak/expense-tracker`).
App Store Connect links here: Support/Marketing URL `https://kishenya.mykoriak.com/`,
Privacy Policy URL `https://kishenya.mykoriak.com/privacy/`.

Plain static files: no JavaScript, no build step. Inter is self-hosted in `fonts/`
(SIL OFL 1.1), so the pages call no third party. Colors follow the app's design system.

## Deploy

GitHub Pages, deployed from `main` / root. Push to `main` and it is live in a minute or two.

- `CNAME` sets the custom domain. Don't delete it.
- DNS at cityhost (controlpanel.host, the mykoriak.com DNS host): `kishenya  CNAME  mykoriak.github.io.`
- HTTPS is enforced in Settings → Pages.

## Keep in sync with the app

When the app changes what data it sends (new provider, account deletion in the app,
the AI consent sheet), update `privacy/index.html` and its "Effective" date, and the
help answers in `index.html`.

## App screenshots

`screens/*.webp` are real captures of the app, not mockups: a Release build on an
iPhone 18 Pro Max simulator (1320 × 2868) with the sample data from
`scripts/demo-backup.mjs` in the app repo, resized to 660 px wide WebP
(`cwebp -q 86 -resize 660 0`). Status bar set to 9:41 with
`xcrun simctl status_bar … override`. For the dark Reports shot the simulator
itself is in dark appearance too. Retake them when the app's screens change.

## Changing `style.css`

GitHub Pages serves files with `cache-control: max-age=600`, so a browser can pair
new HTML with a stale stylesheet for up to ten minutes (on 2026-11-22 that showed
the new screenshots zoomed and cropped). Both pages load `style.css?v=<date>`:
change that `v` in `index.html` and `privacy/index.html` whenever `style.css`
changes.
