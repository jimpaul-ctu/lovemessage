# A Folder for You

A personal, static love-folder website. No server, no backend, no build step — it works anywhere static files can be hosted, including GitHub Pages.

## What's inside

- `index.html` — the entire website (all HTML, CSS, and JavaScript in one file).

The site is fully self-contained:

- The private code lock, letters, tulips page, songs, photo gallery, and love letter maker all run in the browser.
- The "Send to Gmail" button (questions page) and "Send my letter to you" button (letter page) open a Gmail compose window with everything pre-filled. No server is involved, so nothing can break on GitHub Pages.
- Answers and photos are saved only in the visitor's own browser storage.

## Deploying on GitHub Pages

1. Create a new GitHub repository (public).
2. Upload `index.html` to the root of the repository (the file must be named exactly `index.html`).
3. Do NOT upload `server.js`, `package.json`, or `package-lock.json` — GitHub Pages cannot run a Node server, and those files are not needed. If they are already in the repo, delete them.
4. In the repository, go to Settings → Pages.
5. Under "Build and deployment":
   - Source: Deploy from a branch
   - Branch: `main` (or `master`), folder: `/ (root)`
6. Press Save and wait 1–3 minutes.
7. Your site will be live at `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`.

## Updating the site

Edit `index.html`, commit, and push — GitHub Pages redeploys automatically within a couple of minutes.

## Changing the private code

Open `index.html` and find this line near the middle of the file:

```
const PRIVATE_CODE='102926';
```

Change `102926` to any six-digit code you like, then commit and push.

## Where the emails go

Both send buttons open Gmail compose already addressed to orchestratorweb@gmail.com with the content pre-filled — the visitor only presses send. To change the address, open `index.html`, search for `orchestratorweb@gmail.com` (it appears twice), and replace it with your address.

Note: a static site cannot send email by itself with zero clicks — the final "send" press must happen in Gmail. Fully automatic, no-click sending requires a hosted server (e.g. the old `server.js` on Render/Railway with a Gmail App Password).

## Notes

- Spotify embeds require internet access; playback depends on Spotify.
- Very long letters (several thousand characters) may be truncated by Gmail's compose link limit.
