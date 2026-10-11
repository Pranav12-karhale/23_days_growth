# 23-Day Growth OS — Polymathic Learning Edition

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
- PWA manifest and service worker for HTTPS hosting/offline-capable use.

## Run locally

```bash
python -m http.server 8000
```

Open `http://localhost:8000` in your browser.

## Install on Android
Host the folder over HTTPS (for example, GitHub Pages), open its URL in Chrome, then choose **Install app** or **Add to Home screen** from Chrome's menu.

## Data and backup
The app stores progress in the browser's local storage. PC and phone browsers do not sync automatically. Use **Settings → Export JSON** regularly. The export includes schedule times, daily tracking, learning sessions, review queue, mistake log, weekly reviews and editable document content.

## Notes on metrics
Measured scores are domain-specific (for example, DSA independent solve rate vs. a Quant robustness score). Use each domain's own trend over time rather than ranking unlike measures against one another. Confidence calibration compares pre-session prediction with that session's measured outcome.
