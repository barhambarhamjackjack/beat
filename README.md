# Bobby — legal & support site

Five static pages. No build step, no dependencies.

## These files are OUTPUT. Edit the generator.

`../_gensite.py` writes every file in this folder. Editing the HTML directly
works right up until somebody regenerates, and then it silently doesn't.

    python3 _gensite.py

## Why that matters more than it sounds

These pages went three weeks out of date while the app changed underneath them,
and by the end the privacy policy was not merely stale but wrong: it said the
app was called Beat, that there were no accounts, that location was never
collected in the background, that there was no photo or microphone access, and
that map tiles came from CARTO. Every one of those had stopped being true. That
is the document App Store Connect links to, and the one a reviewer reads next to
the app's own permission strings.

So: **when the app changes what it collects, what it shows, or where it sends
anything, this changes in the same batch.** It is not documentation. It is the
promise the app is being judged against.

## Publish on GitHub Pages

1. The repo is `barhambarhamjackjack/beat` — **public**, and separate from the
   private app repo `barhambarhamjackjack/beat-ios`.
2. Upload every file in this folder to the repo root.
3. Repo **Settings → Pages → Source: Deploy from a branch → main / (root)**.

The app points at these URLs (`src/lib/constants.ts`), and they are the URLs in
App Store Connect:

| App Store Connect field | URL |
|---|---|
| Privacy Policy URL | https://barhambarhamjackjack.github.io/beat/privacy.html |
| Support URL | https://barhambarhamjackjack.github.io/beat/support.html |
| Marketing URL (optional) | https://barhambarhamjackjack.github.io/beat/ |

**All three must be live before you submit.** A dead support or privacy URL is
an automatic rejection, and it is the easiest one to avoid.

## A note on these documents

They are written specifically for Bobby as it actually behaves — Sign in with
Apple, anonymous display, moderated user content, foreground location plus
optional rounded background location for nearby alerts, automated screening with
a human behind it, and a UK sole trader as controller.

They are still not legal advice. For a crime-reporting app carrying defamation
and data-protection exposure, an hour with a solicitor before launch is money
well spent — particularly on the liability and moderation sections of the terms.
