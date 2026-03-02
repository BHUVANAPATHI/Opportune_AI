[README (4).md](https://github.com/user-attachments/files/25673527/README.4.md)
# OpportuneAI — Smart Student Opportunity Tracker

> A single-file, AI-powered web application that helps students discover, track, and apply to competitions, hackathons, jobs, internships, scholarships, and more — all in one place.

---

## 🚀 Features

### For Students
| Feature | Description |
|---|---|
| 🏠 **Dashboard** | Overview of matched opportunities, applied events, and AI match score |
| ✨ **My Feed** | Personalized live feed of opportunities based on interests |
| 🏆 **Competitions** | Browse and register for competitions |
| 💡 **Hackathons** | Discover upcoming hackathons |
| 🎓 **Workshops** | Find learning workshops |
| 🔬 **Symposiums** | Explore academic symposiums |
| 💼 **Jobs & Internships** | Browse job and internship listings |
| 🎯 **Scholarships** | Find scholarship opportunities |
| 🤖 **AI Matches** | Claude-powered personalized opportunity recommendations |
| 📄 **Resume Analyzer** | AI-driven resume review and feedback |
| 💬 **AI Assistant** | Conversational AI chatbot for guidance and queries |
| 📋 **Tracker** | Track application status across all opportunities |
| 📊 **Analytics** | Visual insights into your activity and progress |
| 👤 **Profile & Skills** | Manage your profile, skills, and interests |
| ⚙️ **Settings** | Theme, email verification, and account preferences |

### For Organizations
- Org portal with separate login/signup
- Post and manage events
- View registrations and applicant data
- Organization dashboard with stats

---

## 🛠️ Tech Stack

| Category | Technology |
|---|---|
| **Frontend** | Vanilla HTML5, CSS3, JavaScript (no frameworks) |
| **AI** | [Anthropic Claude API](https://api.anthropic.com/v1/messages) — `claude-sonnet` |
| **Fonts** | Google Fonts — Space Grotesk, JetBrains Mono |
| **Storage** | Browser `localStorage` (demo/hackathon mode) |
| **Auth (planned)** | Firebase Authentication |
| **Architecture** | Single Page Application (SPA) — single `.html` file |

---

## 📁 Project Structure

```
OpportuneAI.html        # Entire application in one file
│
├── <script>            # All JavaScript logic
│   ├── DB              # localStorage abstraction layer
│   ├── Auth functions  # Login, Signup, OTP, Forgot Password
│   ├── Nav functions   # SPA screen/page management
│   ├── AI functions    # Claude API calls (matches, resume, chat)
│   └── Org functions   # Organization portal logic
│
├── <style>             # All CSS
│   ├── CSS Variables   # Theming (dark/light mode)
│   ├── Component styles
│   └── Responsive styles
│
└── <body>              # All HTML screens
    ├── Auth Screen     # Student login/signup/OTP
    ├── Org Auth Screen # Organization login/signup
    ├── Student App     # Main SPA with sidebar nav
    └── Org App         # Organization dashboard
```

---

## ⚡ Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Edge, Safari)
- An **Anthropic API Key** (for AI features)

### Running Locally

1. **Clone or download** the project:
   ```bash
   git clone https://github.com/your-username/opportuneai.git
   cd opportuneai
   ```

2. **Open the file** directly in your browser:
   ```bash
   open OpportuneAI.html
   # or just double-click the file
   ```

3. **Add your API Key** — In the app's Settings page, enter your Anthropic API key to enable AI features (AI Matches, Resume Analyzer, AI Assistant).

> No build step, no npm install, no server required. It just works.

---

## 🔑 API Key Setup

OpportuneAI uses the **Anthropic Claude API** for:
- Personalized opportunity matching
- Resume analysis and feedback
- Conversational AI assistant

To get an API key:
1. Visit [console.anthropic.com](https://console.anthropic.com)
2. Create an account and generate an API key
3. Enter the key in the app's ⚙️ Settings page

---

## 🗃️ Data & Storage

In the current demo/hackathon build, all data is stored in **browser localStorage**:

| Key | Data |
|---|---|
| `oai_users` | Registered student accounts |
| `oai_orgs` | Registered organization accounts |
| `oai_session` | Current logged-in session |

> **Note:** Data is local to your browser. Clearing browser storage will reset all accounts. For production, replace the `DB` object's methods with Firebase Auth/Firestore API calls as indicated in the code comments.

---

## 🌗 Theming

OpportuneAI supports **dark and light modes** out of the box, controlled via the `data-theme` attribute on the `<html>` element. Users can toggle themes from the Settings page.

---

## 🔮 Roadmap / Production Upgrades

- [ ] Replace localStorage with **Firebase Firestore**
- [ ] Replace local auth with **Firebase Authentication**
- [ ] Add real **email OTP** via SendGrid or similar
- [ ] Deploy as a hosted web app (Vercel, Netlify, Firebase Hosting)
- [ ] Add Google OAuth for students and organizations
- [ ] Mobile app wrapper (PWA or React Native)

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add your feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** — feel free to use, modify, and distribute.

---

## 🙌 Acknowledgements

- [Anthropic](https://anthropic.com) for the Claude API
- [Google Fonts](https://fonts.google.com) for Space Grotesk & JetBrains Mono
- Built with ❤️ for students, by students
