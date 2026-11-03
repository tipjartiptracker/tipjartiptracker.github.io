# Tip Jar

Free tip tracker for servers and bartenders. Built by servers, for servers.

Everything a person enters stays on their own phone. There's no server, no accounts and no tracking.

## What's in this folder

| File | What it is |
|---|---|
| `index.html` | The app |
| `config.js` | **Your settings**: feedback email, Google Play link, and tip page names |
| `privacy.html` | Privacy policy (link this in Google Play) |
| `manifest.webmanifest` | Lets phones install Tip Jar like an app |
| `sw.js` | Makes Tip Jar work offline |
| `icons/` | App icons |
| `.nojekyll` | Tells GitHub Pages to serve every file as-is. Keep it. |

## Before you publish

1. Open `config.js` and fill in your feedback email and your Venmo / Cash App / PayPal names.
2. After Google Play approves the app, add your Play link to `config.js` to turn on "Rate Tip Jar."

## Updating the app later

Upload the changed files, then open `sw.js` and change `VERSION` (for example `tipjar-1.0.0` to `tipjar-1.0.1`), and change `version` in `config.js` to match. Phones pick up the new version the next time Tip Jar opens with internet.

## Hosting

Host this folder on GitHub Pages in a repository named `yourname.github.io`, so the app lives at the root of the site (`https://yourname.github.io/`). Google Play's app wrapper needs a file at `https://yourname.github.io/.well-known/assetlinks.json`, which PWABuilder gives you when you build the Android app.
