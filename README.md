<div align="center">
  <img src="Assests/cover.png" height="200" />
  <br />
  <img src="Assests/Binge.png" height="80" />

# BingeControl

**Master your watch-time, one challenge at a time — earn the binge, guilt-free.**

[![Hackathon](https://img.shields.io/badge/Built%20at-Thehacktrical%202-orange.svg)](#)
[![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg)](https://opensource.org/licenses/ISC)
[![Stack](https://img.shields.io/badge/Stack-Node%20%7C%20Express%20%7C%20Chrome%20Ext-success)](#tech-stack)

</div>

---

## About

**BingeControl** (originally "Guilt-free Binge") is a Chrome Extension + backend that gamifies self-discipline against streaming-induced procrastination.

|        |                                                                                              |
| ------ | -------------------------------------------------------------------------------------------- |
| Who    | Team **SebastianVettel** — Gyanesh, Eshaan, Sudhanshu, Nitish.                                |
| What   | A credit-economy Chrome extension that meters Netflix watch-time against earned activity.    |
| When   | November 2022, **Thehacktrical 2** hackathon.                                                |
| Where  | Browser-side extension + Node/Express backend with Appwrite + MongoDB.                       |
| Why    | 70% of streaming users binge-watch. Willpower fails — incentives don't.                       |

## The Story

It started with a confession the whole team shared: "one more episode" is a lie we keep telling ourselves at 2 a.m. The numbers backed the gut feeling — Revenge Bedtime Procrastination is now a measurable behavioral pattern, and existing screen-time blockers feel like punishment.

So we built the opposite of a blocker. **BingeControl** treats Netflix time like currency. Finish a quiz, complete a focus session, hit a step goal — credits go up. Open Netflix — credits go down in real time, deducted by an injected content script tracking active playback. Hit zero, and the show pauses until you earn more.

The architecture splits cleanly: a Chrome extension that hooks Netflix's player, an Express API guarding a credit ledger in Appwrite, and Google OAuth so signing in feels like nothing. The team divided up by surface — extension, auth, credit micro-service, UI — and stitched it back together in 36 hours.

The pitch landed because the framing flips guilt into permission: it's not about stopping the binge, it's about **earning the guilt-free pleasure**.

## Gallery

<div align="center">
  <img alt="Preview" src="Assests/preview.png" width="85%" />
</div>

---

## Tech Stack

| Layer        | Tech                                                |
| ------------ | --------------------------------------------------- |
| Frontend     | HTML / CSS / EJS, Chrome Extension APIs              |
| Backend      | Node.js, Express, Passport (Google OAuth)            |
| Data         | Appwrite (credit ledger), MongoDB / Mongoose         |
| Tooling      | nodemon, dotenv, morgan, cors, cookie-session        |

## Repo Structure

```
Thehacktrical-2/
├── Chrome-Extension/   # The browser extension (manifest + popup + injected scripts)
├── api/                # Routes, models, config for the credit & auth services
├── views/              # EJS templates for the web dashboard
├── public/             # Static assets (CSS / JS / images)
├── Assests/            # Branding & preview imagery
├── server.js           # Express entrypoint
├── app.js              # Wiring + middleware
└── play.js             # Playback / credit-deduction helpers
```

## Getting Started

```bash
git clone https://github.com/GyaneshSamanta/Thehacktrical-2.git
cd Thehacktrical-2
npm install

# Create a .env with:
# PORT=3000
# APPWRITE_ENDPOINT=...
# APPWRITE_PROJECT_ID=...
# APPWRITE_KEY=...

npm start
```

Then load the extension:

1. Open `chrome://extensions/`
2. Enable **Developer mode**
3. **Load unpacked** → select the `Chrome-Extension/` folder
4. Sign in via Google and start earning credits.

## Contributing

PRs welcome — fork, branch (`feature/your-thing`), commit, push, open a PR. Issues are a fine place to float ideas before writing code.

## License

ISC. See standard ISC terms.

## Credits

Built at **Thehacktrical 2** by Team SebastianVettel:

- [Gyanesh Samanta](https://github.com/GyaneshSamanta)
- [Eshaan Bhardwaj](https://github.com/Eshaan-B)
- Sudhanshu Srivastava
- Nitish Chaturvedi

<div align="center">
  <a href="https://github.com/GyaneshSamanta/Thehacktrical-2/graphs/contributors">
    <img src="https://contrib.rocks/image?repo=GyaneshSamanta/Thehacktrical-2" />
  </a>
</div>
