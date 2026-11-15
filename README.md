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
