# 🤖 LinkedIn Newsletter Generator

> AI-powered tool that researches real-time industry trends 
> and writes full LinkedIn newsletter articles in your voice.

Part of the [The AI Shift](https://theaishift.co) open source 
toolkit by [Rajeev Nar](https://linkedin.com/in/rajeevnar)

---

## ✨ What It Does

- 🔍 Researches live industry trends from the web in real time
- ✍️ Writes a full structured newsletter article in your voice
- 🎯 Customisable by industry, topic, tone, and length
- 🚀 Outputs LinkedIn-ready copy in seconds
- ⚡ Powered by Claude AI with web search

---

## 🛠️ How to Run It

### Option A — Claude.ai (Easiest, No Setup)
1. Go to [claude.ai](https://claude.ai)
2. Start a new conversation
3. Upload the `app.jsx` file and ask Claude to run it as an artifact
4. The tool loads instantly in your browser

### Option B — Run Locally
1. Make sure you have Node.js installed
   - Check by running `node --version` in your terminal
   - Download from [nodejs.org](https://nodejs.org) if needed

2. Create a new Vite React project:
\```bash
npm create vite@latest newsletter-tool --template react
cd newsletter-tool
npm install
\```

3. Replace `src/App.jsx` with the `app.jsx` file from this folder

4. Create a `.env` file in the root and add your Anthropic API key:
\```
VITE_ANTHROPIC_API_KEY=your_api_key_here
\```

5. Get your API key from [console.anthropic.com](https://console.anthropic.com)

6. Update the fetch headers in `App.jsx`:
\```javascript
headers: {
  "Content-Type": "application/json",
  "x-api-key": import.meta.env.VITE_ANTHROPIC_API_KEY,
  "anthropic-version": "2023-06-01"
}
\```

7. Start the app:
\```bash
npm run dev
\```

8. Open [http://localhost:5173](http://localhost:5173) in your browser

---

## 🔑 Getting Your API Key

1. Go to [console.anthropic.com](https://console.anthropic.com)
2. Sign up or log in
3. Click **API Keys** in the left menu
4. Click **Create Key**
5. Copy and paste into your `.env` file

> ⚠️ Never commit your API key to GitHub. 
> The `.env` file keeps it safe and private.

---

## 📸 Screenshot

![LinkedIn Newsletter Generator](../../docs/screenshots/newsletter-generator.png)

---

## 🏭 Industries Supported

Ecommerce · Marketing · Digital Marketing · SaaS · 
Finance · Healthcare · Education · Manufacturing

---

## 🗂️ Tech Stack

- React (Vite)
- Claude Sonnet API
- Web Search Tool
- Tailwind CSS

---

## 📬 Part of The AI Shift Toolkit

⭐ Star this repo to get notified when new tools drop

Follow **[The AI Shift Newsletter](https://theaishift.co)** 
for the thinking behind each tool.

Built by [Rajeev Nar](https://linkedin.com/in/rajeevnar) 
— Director at [RVS Media](https://rvsmedia.co.uk) 
& Founder of [Velocity AI](https://theaishift.co)
```

4. Scroll down and commit with message:
```
Add README for LinkedIn Newsletter Generator
```

---

## Step 6 — Add a .gitignore File

This protects your API key from ever being accidentally uploaded:

1. Click **Add file → Create new file**
2. Name it exactly:
```
.gitignore
```

3. Paste this:
```
node_modules/
.env
.env.local
.DS_Store
dist/
```

4. Commit with message:
```
Add .gitignore to protect API keys
```

---

## Step 7 — Verify Everything Looks Right

Your repo structure should now look like this:
```
the-ai-shift/
│
├── .gitignore
├── README.md                          ← main repo page
└── marketing/
    └── linkedin-newsletter-generator/
        ├── app.jsx                    ← tool code
        └── README.md                  ← setup guide
