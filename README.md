# Quit Tracker

A small, private, offline web app for cutting back or quitting cigarettes and vaping. No accounts, no server, no tracking. Everything is stored in your browser's local storage on your device.

## Features

- Log vape sessions (with puff count and trigger) and cigarettes
- Daily session cap with a progress bar
- Last-cigarette date and review date, with a status banner
- Device tracker: how long each disposable lasted
- 7-day chart of sessions and cigarettes
- Export to CSV, backup and restore as JSON
- Installs to the home screen and works offline

## Run locally

Service workers need `http://localhost` or HTTPS, so serve the folder rather than opening the file directly:

```
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Publish with GitHub Pages

1. Create a new GitHub repo and push these files to the `main` branch.
2. In the repo, go to **Settings > Pages**.
3. Under **Build and deployment**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, and save.
4. After a minute the app is live at `https://<your-username>.github.io/<repo-name>/`.

## Install on Android

Open the Pages URL in Chrome, open the menu, and choose **Install app** (or **Add to Home screen**). If Chrome doesn't offer to install it, check that both icon files were pushed and reload once so the service worker can register.

## Your data

Data lives in this browser on this device only. Clearing site data deletes it, and each browser or device has its own separate copy. Use **Backup JSON** in Settings now and then, and **Import JSON** to restore.

## Changing the app

After editing any file, change the `CACHE` value in `sw.js` (for example `quit-tracker-v2`) so installed copies pick up the update.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app: markup, styles, and script |
| `manifest.json` | Install metadata |
| `sw.js` | Offline cache |
| `icon-192.png`, `icon-512.png` | App icons |
