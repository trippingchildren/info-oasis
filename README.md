# Info Oasis

A private research browser for Android. Search once, then read articles, studies, books, datasets, and museum collections with no accounts, ads, or search history. It is a plain website (no server, no build step) that people can install to their home screen.

## Files (upload all six)

| File | What it is |
|---|---|
| `index.html` | The whole app |
| `manifest.webmanifest` | Lets Chrome install it as an app |
| `sw.js` | Opens the app fast and offline (stores only the app's own files) |
| `icon-192.png`, `icon-512.png`, `icon-512-maskable.png` | App icons |

## Put it online with GitHub Pages (free)

1. In Chrome, sign in at github.com. Before you start, open **Settings → Emails** and turn on **Keep my email addresses private** and **Block command line pushes that expose my email**.
2. Tap **+ → New repository**. Name it `info-oasis`, choose **Public**, and under **Add license** pick **MIT License**. Create it.
3. On the repo page tap **Add file → Upload files** (if you don't see it, tap ⋮ and choose **Desktop site**). Select all six files, then **Commit changes**.
4. Open **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, pick **main** and **/ (root)**, then **Save**.
5. After a minute or two your app is at `https://YOUR-USERNAME.github.io/info-oasis/`.
6. Open it in Chrome, create your PIN, then tap **⋮ → Install app** (or **Add to Home screen**).

## Let others use it

- **Share the link** from step 5. Anyone can open it and install it to their own phone. Each person sets their own PIN, and nothing is shared between people.
- **Download a copy:** on the repo page tap **Code → Download ZIP**. Those six files can be hosted anywhere.

## Why the repository is public, and what stays private

GitHub Pages is free only for public repositories, and other people can only download from a public one. The repository holds **only the app's code**. Your searches, library, notes, PIN, and settings never go to GitHub: they live on your own phone (see below). A private repository would need a paid GitHub plan for Pages and would stop others from downloading.

## What is stored on a phone

Only a scrambled copy of the PIN, plus theme, text size, language, and auto-lock choice, kept in the browser's local storage under keys that start with `infooasis.`. No history, searches, or library are stored. Your Library lives in memory; use **Export file** to keep it.

## Using it

- **First time:** create a 4 to 8 digit PIN. After that it asks for the PIN every time you open it.
- **All settings** (PIN, auto-lock, theme, text size, language, Safe Search): the sliders button at the top.
- **Safe Search** is on at every launch. Turn it off (18+) in **Settings** for that visit only; a small "18+ on" badge shows at the top while it is off.
- **Forgot your PIN:** tap **Forgot PIN?** on the lock screen. This erases the PIN and settings and clears the session.

## Good to know

- Anyone with the link can open the app. The PIN keeps people who pick up a phone out of it; it is a lock on the page, not encryption.
- GitHub can see that the page was loaded, and each source searched sees the IP address and the search. See the Privacy and Sources pages inside the app.
- Some sources may not allow requests from a web page. When that happens the results page says some sources couldn't be reached and shows the rest.
- **Updating:** upload the changed files again (commit over the old ones). If the old version keeps showing, change `CACHE` in `sw.js` (for example to `info-oasis-v2`) and reload twice.
- The page includes a `noindex` tag so search engines are asked not to list it.
- Info Oasis is not affiliated with the Wikimedia Foundation or any source it searches.
