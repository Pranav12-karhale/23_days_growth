# Growth OS — Polymathic Learning Edition

A mobile-friendly, local-first web app/PWA for the 14 Oct 2026 → 5 Nov 2026 sprint.

## Features
- Redesigned daily schedule: planning/retrieval warm-up, AI/ML deep work first, DSA second, CS Fundamentals, System Design, Quant, Projects/Research and metacognitive review.
- Editable daily operating schedule with custom start/end times, automatic duration calculation, overlap warnings, save/reset/cancel.
- Daily tracker with tasks, 0–2 domain scores, sleep, focus hours, wins and mistakes.
- Learning Lab with editable topic/objective, confidence before and after, an outcome metric, and evidence/artifact notes per domain.
- Automatic spaced-review queue for saved topics (+1, +3 and +7 days), including due/overdue review notes and completion tracking.
- Persistent mistake/insight log with topic, root cause, corrective action, search/filter, editing and reviewed status.
- Weekly Review pages with focus hours, scores, task completion, measured-session counts and editable metacognitive reflections.
- Analytics for score/focus trends, task completion, per-domain measured outcome history and confidence calibration.
- Original Word-plan content retained in the editable Full Plan section.
- Local data-aware Coach Chat, JSON export/import and browser localStorage persistence.
- Installable PWA setup: manifest, 192px/512px app icons (including maskable icons), HTTPS-ready service worker and offline app-shell caching.

## Run locally for testing

```bash
python -m http.server 8000
```

Open `http://localhost:8000` in Chrome. `localhost` is treated as a secure development origin, so PWA features can be tested locally on the computer. This does not make the computer's localhost URL accessible from your Android phone.

## Install on Android (important)

A PWA must be hosted on an **HTTPS URL** to install on Android (except a localhost development environment). Opening `index.html` as a local file, or sharing the HTML file directly to your phone, will generally only offer a browser shortcut rather than app installation.

### GitHub Pages steps
1. Extract the complete ZIP.
2. Upload **all contents** of `23_day_growth_tracker_app` to the root of your GitHub repository. Do not upload only `index.html`. The repository must contain `index.html`, `manifest.webmanifest`, `sw.js`, and the entire `icons/` folder.
3. In GitHub, open **Settings → Pages** and publish from the `main` branch and the repository root (`/`).
4. Wait for deployment to finish. Open the resulting `https://<username>.github.io/<repository>/` URL on Android in Chrome.
5. Reload the page once. Open Chrome's `⋮` menu and look for **Install app**. The button labelled **Install app** in the app header can also trigger the install prompt when Chrome makes it available.
6. If you previously created a shortcut, remove that shortcut, redeploy all updated files, close the old tab, reopen the HTTPS URL, and reload it. If Chrome still offers only a shortcut, check the URL is HTTPS and verify these paths load on your phone: `/manifest.webmanifest`, `/sw.js`, and `/icons/icon-192.png` (keep the repository subpath in each URL if using GitHub Pages).

Install-menu wording and availability are controlled by Chrome and can vary by device/version. The correct PWA files are included here, but this ZIP itself cannot publish the app to a public URL.

## Data and backup
The app stores progress in the browser's local storage. PC and phone browsers do not sync automatically. Use **Settings → Export JSON** regularly. The export includes schedule times, daily tracking, learning sessions, review queue, mistake log, weekly reviews and editable document content.

## Notes on metrics
Measured scores are domain-specific (for example, DSA independent solve rate vs. a Quant robustness score). Use each domain's own trend over time rather than ranking unlike measures against one another. Confidence calibration compares pre-session prediction with that session's measured outcome.
