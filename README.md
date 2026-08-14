📚 Cognixia – Shaping Tech Minds

A Modern, Offline‑First E‑Learning Platform for ICT Skills

https://img.shields.io/badge/License-MIT-blue.svg
https://img.shields.io/badge/Made%20with-JavaScript-F7DF1E.svg
https://img.shields.io/badge/PWA-Ready-5A0FC8.svg
https://img.shields.io/badge/Offline-Supported-27ae60.svg

---

🌟 Overview

Cognixia is a feature‑rich, offline‑first learning platform designed for ICT and tech education. Learners can access courses, watch video lessons, complete interactive quizzes, earn certificates, and track their progress – all without an internet connection once loaded.

The platform is built entirely with vanilla JavaScript, IndexedDB for client‑side storage, and follows Progressive Web App (PWA) best practices, making it installable on any device.

assets/screenshots/dashboard.png <!-- Replace with actual screenshot -->

---

🚀 Key Features

Feature Description
🔐 Authentication User registration, login, and session management with password hashing (PBKDF2) and per‑user salts
📚 Course Management Browse, filter, and enroll in ICT courses across multiple categories
🎬 Video Lessons Watch YouTube or MP4 videos with automated progress tracking (≥80% watched = lesson complete)
📝 Quizzes Multiple‑choice quizzes with detailed explanations, passing thresholds, and automatic scoring
🏆 Certificates Generate professional, downloadable certificates upon course completion (PNG/PDF)
📊 Progress Tracking Dashboard with course completion, lesson progress, streaks, and learning time
🔥 Progress Heatmap GitHub‑style activity calendar showing daily learning habits
🧠 Smart Recommendations Personalized course suggestions based on completed courses and interests
🗺️ Learning Paths Curated career tracks (Full Stack, Cybersecurity, Data Science)
💻 Code Playground Live HTML/CSS/JS editor with save, load, and delete snippets
🌐 Virtual Network Lab Interactive network simulator with packet tracing and topology visualization
📱 Mobile‑First PWA Installable on any device, works offline with service worker caching
🎨 Modern UI Clean, responsive design with light/dark theme, avatar initials, and smooth animations

---

🛠️ Technologies Used

Core Stack

· HTML5 – Semantic markup
· CSS3 – Flexbox, Grid, custom properties, responsive design
· JavaScript (ES6+) – Vanilla JS, no frameworks

Storage & Offline

· IndexedDB – Client‑side database for user data, progress, courses, and snippets
· Service Worker – Caches assets for offline access

Security

· Web Crypto API – PBKDF2 with per‑user salts for password hashing
· Session Tokens – Cryptographically secure UUIDs

Libraries (loaded on demand)

· Chart.js – Progress charts
· html2canvas – Certificate generation (PNG)
· jsPDF – Certificate export (PDF)
· YouTube IFrame API – Video progress tracking

PWA

· Web App Manifest – Installable on mobile devices
· Service Worker – Offline caching and network fallback

---

📂 Project Structure

```
cognixia/
├── index.html              # Main dashboard
├── login.html              # Login page
├── register.html           # Registration page
├── course-player.html      # Course player with video & quiz
├── auth.js                 # Authentication logic (users, sessions, password hashing)
├── courses.js              # Course data with quizzes, videos, and learning paths
├── script.js               # Main application logic
├── style.css               # Global styles
├── auth.css                # Authentication page styles
├── sw.js                   # Service worker for PWA
├── manifest.json           # PWA manifest
├── assets/
│   ├── images/
│   │   ├── cognixia-logo.png    # Platform logo
│   │   └── favicon.ico          # Favicon
│   └── screenshots/             # Screenshots for README
├── LICENSE
└── README.md
```

---

🚀 Getting Started

Prerequisites

· A modern web browser (Chrome, Edge, Firefox, or Safari)
· No server required – works as static files

Local Development

1. Clone the repository
   ```bash
   git clone https://github.com/yourusername/cognixia.git
   cd cognixia
   ```
2. Open the application
   · Double‑click index.html to open in your browser, or
   · Use a local development server (recommended):
     ```bash
     # Using Python 3
     python3 -m http.server 8000
     
     # Using Node.js (if you have npx)
     npx serve .
     ```
   · Visit http://localhost:8000 in your browser
3. First‑time setup
   · Register a new account – the admin user is automatically seeded.
   · The database is created automatically in your browser's IndexedDB.

Production Deployment

You can deploy Cognixia to any static hosting service:

Platform Instructions
GitHub Pages Push to a repository, enable Pages from the main branch
Netlify Drag‑and‑drop the project folder or connect your repo
Vercel Deploy with vercel CLI or connect your GitHub repo
Any Web Server Upload the files to your web server's public directory

Important: Ensure your server serves sw.js and manifest.json from the root directory for PWA functionality.

---

🧪 Default Accounts

The platform seeds an admin account on first run:

Email Password Role
admin@cognixia.com Admin123! Administrator

You can register new student accounts via the registration page.

---

📖 Usage Guide

For Learners

1. Register – Create a new account using your email and a strong password.
2. Log in – Access your personalized dashboard.
3. Browse Courses – Explore ICT courses across categories (Programming, Networking, Cybersecurity, Web Development).
4. Start Learning – Click "Start Course" to open the course player.
5. Watch Videos – Each lesson includes a video; progress is tracked automatically.
6. Complete Lessons – Mark lessons as complete manually, or watch ≥80% of the video to auto‑complete.
7. Take Quizzes – After all lessons are complete, unlock the quiz. Pass to earn a certificate.
8. Earn Certificates – Generate and download your certificate as PNG or PDF.
9. Track Progress – View your heatmap, streaks, and completion stats on the dashboard.

---

🎓 Learning Paths

Cognixia includes curated learning paths to guide learners toward specific career goals:

Path Courses Included
Full Stack Developer Web Development Fundamentals, JavaScript Advanced, Database Management
Cybersecurity Analyst Cybersecurity Fundamentals, Networking Essentials
Data Scientist Python Programming Basics, Database Management

Paths are displayed on the dashboard and track completion automatically.

---

🔐 Security

· Password Hashing – Uses PBKDF2 with 100,000 iterations and per‑user random salts.
· Session Management – Secure UUID tokens with configurable expiry (30 minutes / 7 days with "Remember Me").
· Local Storage – All data is stored in IndexedDB; no data is sent to external servers.
· XSS Prevention – User‑generated content is sanitized where displayed.

---

📱 PWA & Offline Support

Cognixia is a fully installable Progressive Web App:

· Installation – On mobile, tap "Add to Home Screen"; on desktop, use the browser's install prompt.
· Offline Mode – Once visited, the app works without an internet connection.
· Service Worker – Caches all static assets (HTML, CSS, JS, images) for fast loading.
· Auto‑Sync – Progress is saved locally; data persists across sessions.

---

🤝 Contributing

We welcome contributions! Here's how you can help:

1. Fork the repository
2. Create a feature branch
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. Make your changes – follow the existing coding style.
4. Test – ensure the platform works offline and all features are functional.
5. Commit – write clear, descriptive commit messages.
6. Push – push your branch to your fork.
7. Open a Pull Request – describe your changes and why they're valuable.

Contribution Guidelines

· Keep the code vanilla – no frameworks or heavy dependencies.
· Ensure backward compatibility with older browsers (except where PWA APIs are used).
· Document new features in the README.
· Test across mobile, tablet, and desktop viewports.
· Follow semantic HTML and accessible practices.

---

🐛 Reporting Issues

Found a bug? Please open an issue with:

· Description – What happened and what you expected.
· Steps to Reproduce – Detailed steps to reproduce the issue.
· Browser/Device – Your browser, version, and device type.
· Screenshots – If applicable, add screenshots to help explain the problem.

---

🧠 Future Roadmap

☐ AI‑Powered Tutor – Personalized learning assistance via ChatGPT integration.
☐ Social Features – Study groups, course‑level discussions, peer Q&A.
☐ Employer‑Ready Profiles – Shareable progress cards and resume builder.
☐ Gamified Duels – Live 1v1 quiz battles and leaderboards.
☐ Project Portfolio – GitHub integration to showcase completed projects.
☐ Multi‑Language Support – i18n for global reach.

---

📄 License

This project is licensed under the MIT License – see the LICENSE file for details.

---

🙏 Acknowledgments

· Icons – Font Awesome
· Fonts – Google Fonts (Poppins)
· Charting – Chart.js
· PDF Generation – jsPDF
· Screenshot Capture – html2canvas
· YouTube Integration – YouTube IFrame API

---

📧 Contact

· Project Maintainer – Kelvin Mwichwiri
· GitHub – https://github.com/kelvin7331/cognixia

---

⭐ Show Your Support

If you find Cognixia useful, please give it a ⭐ on GitHub! Your support helps us continue improving the platform.

---

Cognixia – Empowering the next generation of tech talent, one lesson at a time. 🚀