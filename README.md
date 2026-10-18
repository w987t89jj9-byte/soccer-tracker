# Soccer Team Tracker V1.4 — GitHub Pages PWA

A standalone, mobile-friendly soccer stat tracker for **your team only**, with 9v9/11v11, 30/35/40/45-minute halves, individual stats, game clock, playing time, and single/bulk substitutions.

## Publish in one batch
1. On GitHub, create a **public** repository named `soccer-tracker` (do not add a README when creating it).
2. Open the repository, choose **Add file → Upload files**, and upload the **contents of this ZIP** into the repository root, preserving the `icons` folder. Commit the files.
3. Go to **Settings → Pages**. Under **Build and deployment**, select **Deploy from a branch**, branch **main**, folder **/(root)**, then **Save**.
4. Wait for Pages to publish, then open `https://YOUR-USERNAME.github.io/soccer-tracker/` (replace YOUR-USERNAME).
5. On your phone, open that URL. iPhone Safari: Share → Add to Home Screen. Android Chrome: menu → Install app / Add to Home screen.

## Data and backups
- Game data is stored in the browser on each device; it **does not sync** between devices.
- Data from an HTML file opened directly on your computer will **not automatically transfer** to the GitHub Pages website. Export JSON from the old app and import it on the hosted site.
- Export JSON after each game. Clearing browser/site data can delete saved games.
- The service worker caches the app for offline use **after the first successful online visit**. Test offline mode before a real game.
- Browser clock recovery uses timestamps. Test the phone's screen lock/background behavior before relying on it at a game.
- GitHub Pages on a public repository publishes these app files publicly, **not** your locally stored roster or game data. Do not commit game export JSON files if you want to keep them private.

## Updating
Upload changed files to the repository and commit. When updating the service worker, change the CACHE name to ensure an updated offline cache. Reload the site online to receive updates.

V1.4: Touch selection for events, team-only Goals Allowed, game events CSV.

## V1.4 changes
- Goals Allowed now prompts for goalkeeper selection, counted in individual and team totals and player CSV.
- Old V1.3 exports with a `goalkeeper` field are recognized and normalized on import.
- Existing storage key and game IDs remain unchanged; import same-ID game replaces it.
- Import the separately supplied corrected October 18 JSON for the requested historical adjustment.
