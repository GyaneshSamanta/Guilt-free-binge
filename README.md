<div align="center">
  <img src="Assests/cover.png" height="180" />
  <br />
  <img src="Assests/Binge.png" height="80" />
  <h1>🚀 BingeControl</h1>
  <p><b>Master your watch-time, one challenge at a time.</b></p>

[![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg)](https://opensource.org/licenses/ISC)
[![Made with Coffee](https://img.shields.io/badge/Made%20with-☕-brown.svg)](#)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/GyaneshSamanta/Thehacktrical-2/pulls)
[![Hackathon](https://img.shields.io/badge/Built%20at-Thehacktrical%202-orange.svg)](#)

</div>

<hr />

## 🎬 The "Why" (PM Perspective)

**The Problem:** Binge-watching is the silent productivity killer of our generation. 70% of Netflix users binge-watch, often resulting in "Revenge Bedtime Procrastination" and a total loss of accountability.

**The Solution:** **BingeControl** gamifies self-discipline. Instead of relying on raw willpower (which fails), we introduce a **Credit-based Reward System**. You want an hour of _Stranger Things_? Earn it by completing physical or mental micro-tasks.

> "It's not about stopping the binge; it's about earning the guilt-free pleasure."

### 📈 Success Metrics (KPIs)

- **Time Reclaimed**: Average weekly reduction in hours spent on streaming platforms.
- **Conversion Rate**: Number of units of "Work" (tasks) converted into "Play" (watch time).
- **Engagement Retention**: Percentage of users who stay within their credit limit for 7+ consecutive days.

---

## ✨ Features

- 🛠️ **Seamless Integration**: A lightweight Chrome Extension that lives right where you watch.
- 💰 **Credit Economy**: Earn credits through activity modules and spend them to "unlock" watch time.
- 📊 **Real-time Tracking**: Automatic session monitoring that deducts credits as you watch.
- 🛑 **Enforced Breaks**: When your credits hit zero, it's time to get up and earn more!

---

## 🛠️ Tech Stack (Developer Perspective)

| Category     | Technology                 | Purpose                                               |
| :----------- | :------------------------- | :---------------------------------------------------- |
| **Frontend** | ReactJS + HTML/CSS         | Modern, responsive UI for the extension & dashboard.  |
| **Backend**  | ExpressJS + NodeJS         | Scalable API handling credits and authentication.     |
| **Database** | Appwrite + MongoDB         | Cloud-based credit storage & user profile management. |
| **Auth**     | Passport.js (Google OAuth) | Frictionless sign-ins for users.                      |
| **Client**   | Chrome Extension API       | In-browser script injection for Netflix tracking.     |

---

## 🏗️ System Architecture

1.  **Extension**: Injects a script into Netflix to track active video playback.
2.  **API Gateway**: `server.js` routes requests to auth and credit handlers.
3.  **Credit Micro-service**: Uses Appwrite's database to atomically update user credits based on "Work" (score) vs "Play" (watch time).
4.  **Security**: Middleware ensures users can only spend the credits they've earned.

---

## 🔌 API Reference (Internal)

| Endpoint                | Method | Description                                |
| :---------------------- | :----- | :----------------------------------------- |
| `/api/credits/fetchAll` | `GET`  | Fetches all user credit profiles.          |
| `/api/credits/score`    | `POST` | Increments credits (User finished a task). |
| `/api/credits/stop`     | `POST` | Decrements credits (User is watching).     |
| `/auth/google`          | `GET`  | Initiates Google OAuth flow.               |

---

## 🚀 Setting Up the Lab

### 1. Backend Initialization

```bash
# Clone the repository
git clone https://github.com/GyaneshSamanta/Thehacktrical-2.git
cd Guilt-free-binge

# Install dependencies
npm install

# Setup Environment Variables (.env)
PORT=3000
APPWRITE_ENDPOINT=your_endpoint
APPWRITE_PROJECT_ID=your_id
APPWRITE_KEY=your_key

# Start the engine
npm start
```

### 2. Chrome Extension Setup

1. Open Chrome and head to `chrome://extensions/`.
2. Toggle **Developer Mode** (top right).
3. Click **Load unpacked**.
4. Select the `Chrome-Extension` folder from this repository.
5. Pop open the extension and sign in!

---

## 📸 Preview

<div align="center">
  <img alt="Preview Images" src="Assests/preview.png" width="80%" />
</div>

---

## 🗓️ Roadmap (Product Vision)

- [ ] **Multi-platform Support**: Support for Prime Video, Disney+, and Hulu.
- [ ] **Social Leaderboards**: Compete with friends on who has the best "Self-Control Score".
- [ ] **Hardcore Mode**: Integration with smart locks/smart plugs to physically lock distractions.
- [ ] **Advanced Analytics**: Monthly reports on how many hours of life you "saved".

---

## 🤝 Contributing

We love developers who want to help users reclaim their time!

1. **Fork** the project.
2. Create your **Feature Branch** (`git checkout -b feature/AmazingFeature`).
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`).
4. **Push** to the branch (`git push origin feature/AmazingFeature`).
5. Open a **Pull Request**.

---

## 📜 License & Disclaimers

Distributed under the **ISC License**.

_Note: This project was built during Thehacktrical 2 hackathon. Plagiarism is uncool—if you use this code, give the team some credit!_

<div align="center">
  <h3>Built with ❤️ by Team SebastianVettel</h3>
  <a href="https://github.com/GyaneshSamanta/Thehacktrical-2/graphs/contributors">
    <img src="https://contrib.rocks/image?repo=GyaneshSamanta/Thehacktrical-2" />
  </a>
</div>
