# Daily Commit Challenge Tracker 🚀

A dynamic, automated billboard to publicly track my daily coding journey. This single‑page application fetches live commit history from the GitHub API and visualizes progress, streaks, and achievements on a clean, modern interface.

<p align="center">
  <a href="https://YOUR-NETLIFY-URL.netlify.app" target="_blank"><b>✨ View the Live Demo ✨</b></a>
  <br/>
  <sub>(Replace the link above with your actual Netlify URL)</sub>
</p>

---

## 🎯 About The Challenge
Consistency is key in software development. To build a strong habit of coding every day, improve skills, and create a portfolio from scratch, I’ve committed to this public challenge. This tracker serves as my personal accountability partner and a public billboard of my dedication.

Follow along with my progress!

---

## 🌟 Features
- **📈 Live Data from GitHub** — Automatically fetches and displays public commit history (no manual updates).
- **🗓️ Interactive Calendar** — Highlights days with commits across the current month.
- **🔥 Streak Calculation** — Current and longest streaks, updated in real‑time.
- **🏆 Achievements System** — Unlock milestones (e.g., 7‑day streak, full month complete).
- **📊 At‑a‑Glance Stats** — Latest activity, recent commit messages, monthly progress.
- **👤 Dynamic Profile** — Pulls GitHub avatar, name, and bio automatically.
- **⚡ Fully Automated** — Set your username once; the app handles the rest.

---

## 📸 Sneak Peek
> _Tip: Take a screenshot of your deployed app and replace the placeholder below._

![App Screenshot Placeholder](./screenshot.png)

---

## 🛠️ Tech Stack
- **HTML5** — Single‑file structure (no build steps required)
- **Tailwind CSS** — Utility‑first styling for a modern UI
- **JavaScript (ES6+)** — API calls, state management, DOM rendering

---

## 🧠 How It Works
1. **API Fetching** — On page load, the app requests the public GitHub Events API:
   - `https://api.github.com/users/<YOUR_USERNAME>/events/public`
2. **Data Processing** — Filters `PushEvent` items to identify commit dates and messages.
3. **State Calculation** — Calculates daily activity, current streak, longest streak, and achievements.
4. **Dynamic Rendering** — Injects computed state into the calendar grid and stat cards.
5. **(Optional) Caching** — Stores the last successful response and computed state in `localStorage` to reduce API calls.

> ℹ️ **API Notes**
> - Unauthenticated requests are rate‑limited (typically **60 req/hour per IP**). If you expect higher traffic, consider adding optional authentication with a GitHub **Personal Access Token** (PAT) to lift limits (up to **5,000 req/hour**).
> - The Events API surfaces recent activity; very old commits may require pagination or using the GraphQL API for contribution calendars.

---

## 📂 Project Structure
This project is a single, portable file.
```
.
└── challenge_tracker.html     # Open directly in your browser
```

---

## ⚙️ Configuration
Open `challenge_tracker.html` and set your GitHub username near the top of the `<script>` tag:

```js
const config = {
  githubUsername: 'reddybalajimadha',
  // Optional: supply a GitHub token via query param or localStorage for higher rate limits
  // githubToken: null
};
```

**Optional token usage (dev only):**
- Temporarily store a token in `localStorage.setItem('gh_token', 'YOUR_TOKEN')` and have the app read it.
- Never commit personal tokens to the repo.

---

## 🧪 Running Locally
1. **Clone this repo**
   ```bash
   git clone https://github.com/<your-username>/<your-repo>.git
   cd <your-repo>
   ```
2. **Open the app**
   - Double‑click `challenge_tracker.html`, or
   - Serve it (optional) with a simple server:
     ```bash
     # Python 3
     python -m http.server 5500
     # Then visit http://localhost:5500/challenge_tracker.html
     ```

---

## ☁️ Deploy
**Netlify (recommended)**
1. Create a new site from Git in Netlify and select this repository.
2. Build settings: _none required_ (static file).
3. Deploy. Replace the demo link at the top with your Netlify URL.

**GitHub Pages**
1. Push the repo to GitHub.
2. Enable **Pages** for the repo (branch: `main`, folder: `/root`).
3. Access the page at `https://<your-username>.github.io/<your-repo>/challenge_tracker.html`.

---

## 🔥 Streaks & 🏆 Achievements
**Streak rules**
- A day counts if there’s ≥1 commit on that calendar date (UTC or your chosen timezone).
- Current streak: consecutive commit days ending **today**.
- Longest streak: max over entire fetched history.

**Default achievements (editable in code):**
- 🎯 First Commit Day
- 🔥 3‑Day Streak
- 🔥 7‑Day Streak
- 🔥 14‑Day Streak
- 🔥 30‑Day Streak
- 📅 Full Month Completed (commit on every day of a calendar month)
- 💯 100 Commits Logged
- 🧱 No‑Zero Month (no zero‑commit days in a month)

> Customize achievements in the `achievements` array for your personal goals.

---

## 🔐 Privacy & Permissions
- The app only reads **public** activity from the GitHub API.
- If you add token support for higher rate limits, store tokens locally and **do not** commit them.

---

## 🧩 Customization Ideas
- **Timezone control** (e.g., force `America/Los_Angeles` for streak calculation)
- **Theme switcher** (light/dark/system)
- **Animation polish** (celebrate achievements)
- **Graph view** (weekly commit bar chart)
- **Export badge** (auto‑generate a README badge with current streak)

---

## 🐛 Troubleshooting
- **Nothing shows up** — Confirm the `githubUsername` is correct and you have recent public `PushEvent`s.
- **Rate‑limited** — Add optional token support or enable result caching.
- **Old commits missing** — The Events API focuses on recent activity; consider pagination or GraphQL for broader history.

---

## 🗺️ Roadmap
- [ ] Add month/year navigation
- [ ] Persist computed state to `localStorage` with TTL
- [ ] Add bar/line charts for per‑week activity
- [ ] Add GraphQL option for contribution calendar
- [ ] Publish as a lightweight web component

---

## 🤝 Contributing
Contributions welcome! Please open an issue to discuss major changes.

---

## 📄 License
This project is licensed under the **MIT License**. See `LICENSE` for details.

---

## 🙌 Acknowledgments
- GitHub REST API / Events API
- Tailwind CSS

---

## 👋 Get In Touch
**Your Name:** _Add your name here_

**GitHub:** [@reddybalajimadha](https://github.com/reddybalajimadha)

**LinkedIn:** _Add your LinkedIn profile URL here_

---

### ⭐ If this project helps you, consider starring the repo!

