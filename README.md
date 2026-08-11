# Bobby — legal & support site

Five static pages. No build step, no dependencies. Publishing takes about five minutes.

## Publish on GitHub Pages

1. Create a **public** repo called `beat` at github.com/new
2. Upload every file in this folder to the repo root (drag and drop works)
3. Repo **Settings → Pages → Source: Deploy from a branch → main / (root) → Save**
4. Wait about a minute, then check https://barhambarhamjackjack.github.io/beat/

The app already points at these URLs (`src/lib/constants.ts`), and they are the
URLs to give App Store Connect:

| App Store Connect field | URL |
|---|---|
| Privacy Policy URL | https://barhambarhamjackjack.github.io/beat/privacy.html |
| Support URL | https://barhambarhamjackjack.github.io/beat/support.html |
| Marketing URL (optional) | https://barhambarhamjackjack.github.io/beat/ |

**All three must be live before you submit.** A dead support or privacy URL is
an automatic rejection, and it is the easiest one to avoid.

## If you later buy a domain

Point it at the repo (Settings → Pages → Custom domain), then update the three
constants in `src/lib/constants.ts` and resubmit. Nothing else changes.

## A note on these documents

They are written specifically for Bobby as it actually behaves — anonymous
device IDs, moderated user content, optional foreground-only location, a UK
sole trader as controller. They are not a generic template, and the App Store
sections match what the app really does.

They are still not legal advice. For a crime-reporting app carrying defamation
and data-protection exposure, an hour with a solicitor before launch is money
well spent — particularly on the liability and moderation sections of the terms.
