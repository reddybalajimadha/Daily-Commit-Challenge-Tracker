Daily Commit Challenge Tracker 🚀
A dynamic, automated billboard to publicly track my daily coding journey. This single-page application fetches my live commit history from the GitHub API and visualizes my progress, streaks, and achievements on a clean, modern interface.

✨ View the Live Demo Here! ✨
(Don't forget to replace the link above with your actual Netlify URL!)

🎯 About The Challenge
Consistency is key in software development. To build a strong habit of coding every day, improve my skills, and create a portfolio from scratch, I've committed to this public challenge. This tracker serves as my personal accountability partner and a public billboard of my dedication.

Follow along with my progress!

🌟 Features
📈 Live Data from GitHub: Automatically fetches and displays my public commit history. No manual updates needed!

🗓️ Interactive Calendar: A full monthly calendar that visually highlights all days a commit was made.

🔥 Streak Calculation: Dynamically calculates my current and longest commit streaks to keep me motivated.

🏆 Achievements System: Unlocks achievements for milestones like hitting a 7-day streak or completing a full month.

📊 At-a-Glance Stats: Clean, card-based UI to show latest activity, recent commit messages, and monthly progress.

👤 Dynamic Profile: Pulls my GitHub profile picture, name, and bio automatically.

⚡ Fully Automated: Set the username once and the application runs itself.

📸 Sneak Peek
(Tip: Take a screenshot of your deployed app and replace this placeholder image.)

🛠️ Tech Stack
This project is built with a focus on simplicity and performance, using vanilla web technologies:

HTML5: For the core structure and content.

Tailwind CSS: For modern, utility-first styling.

JavaScript (ES6+): For all the logic, including API calls, state management, and DOM manipulation.

⚙️ How It Works & Local Setup
The application is a single index.html file with no build steps required.

API Fetching: On page load, the JavaScript makes a fetch request to the public GitHub Events API (https://api.github.com/users/YOUR_USERNAME/events/public).

Data Processing: It parses the event data, filtering for PushEvent types to identify commit dates.

State Calculation: Based on the commit dates, it calculates streaks, achievements, and statistics.

Dynamic Rendering: The script then injects all this information into the HTML to render the calendar and stats.

To run this project locally, simply clone the repository and open the challenge_tracker.html file in your web browser.

Configuration
The only configuration needed is to set your GitHub username. Open the challenge_tracker.html file and find this line in the <script> tag:

const config = {
    githubUsername: 'YOUR_USERNAME_HERE' 
};

Replace 'YOUR_USERNAME_HERE' with your GitHub username, and you're all set!

👋 Get In Touch
Your Name: [Your Name Here]

GitHub: reddybalajimadha

LinkedIn: (Add your LinkedIn profile URL here)

Thanks for checking out my project!
