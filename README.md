# Daily Commit Challenge Tracker

A single-file billboard that auto-pulls your **public** GitHub activity and shows a calendar, streaks, achievements, and recent commits—no manual input.

**Quick Start**
1. Open `index.html` and set `githubUsername` in the `<script>` (e.g., `'reddybalajimadha'`).
2. Open the file in a browser, or deploy:
   - **Netlify:** drag-and-drop `index.html`
   - **GitHub Pages:** enable Pages on the repo and visit the URL

**Notes**
- Counts **PushEvents** from public repos only (private activity won’t appear).
- GitHub unauthenticated API is rate-limited (~60 req/hr/IP).

**Live Site:** _reddy-balaji-daily-challenge-tracker.netlify.app_
