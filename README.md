# 💬 Gemini Chat

A beautiful, free AI chatbot powered by **Google Gemini 1.5 Flash** — deployable to GitHub Pages in minutes. No backend, no server, no cost.

---

## ✨ Features

- 🤖 **Powered by Google Gemini 1.5 Flash** — fast, smart, and free
- 💸 **100% Free** — no credit card, no billing, no API cost
- 🌐 **Single HTML file** — no frameworks, no build tools, no dependencies
- 💬 **Multi-turn conversation** — remembers full chat history
- 📝 **Markdown rendering** — supports code blocks, bold, italic
- ⚡ **Typing animation** — real-time visual feedback
- 📱 **Responsive** — works on desktop and mobile
- 🔐 **Secure** — API key stored in memory only, never saved

---

## 🚀 Deploy to GitHub Pages (2 minutes)

### Step 1 — Create a GitHub repo
1. Go to [github.com](https://github.com) and sign in
2. Click **+** → **New repository**
3. Name it `gemini-chat` (or anything you like)
4. Click **Create repository**

### Step 2 — Upload the file
1. On your repo page, click **"uploading an existing file"**
2. Drag and drop `index.html`
3. Click **Commit changes**

### Step 3 — Enable GitHub Pages
1. Go to **Settings** → **Pages** (left sidebar)
2. Under Branch, select **main** → **/ (root)**
3. Click **Save**

### Step 4 — Open your live site
After ~60 seconds, your chatbot is live at:
```
https://YOUR_USERNAME.github.io/gemini-chat
```

---

## 🔑 Getting Your Free Gemini API Key

1. Go to [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)
2. Sign in with your Google account
3. Click **Create API Key**
4. Copy the key (starts with `AIza...`)
5. Paste it into the chatbot on first launch

> **No credit card required.** Free tier includes 15 requests/minute.

---

## ⚠️ Important: Local vs Deployed

| Environment | Works? | Why |
|---|---|---|
| `file://` (opened from Downloads) | ❌ No | Browser blocks API calls from local files |
| `localhost` (Python server) | ✅ Yes | Treated as a real server |
| GitHub Pages (`https://...`) | ✅ Yes | Real HTTPS website |

**To test locally** before deploying:
```bash
# In the folder containing index.html
python -m http.server 8080
# Then open http://localhost:8080
```

---

## 🛠️ Customization

Open `index.html` in any text editor and modify:

| What | Where in file |
|---|---|
| Change AI model | `var model = 'gemini-1.5-flash'` |
| Change placeholder text | `placeholder="Ask Gemini anything..."` |
| Change page title | `<title>Gemini Chat</title>` |
| Change accent color | `--accent: #1a73e8` in `:root` |
| Add a system prompt | Modify the `callGemini()` function body |

---

## 📁 Project Structure

```
gemini-chat/
└── index.html    ← Everything in one file
```

---

## 🧠 How It Works

1. User enters their Gemini API key (stored in memory only)
2. Each message is sent to the Gemini API along with full conversation history
3. The response is rendered with basic Markdown support
4. The conversation history grows with each turn, enabling context-aware replies

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

## 🙋 FAQ

**Q: Is it really free?**  
A: Yes. Google's free tier for Gemini 1.5 Flash allows 15 requests/minute and 1 million tokens/day at no cost.

**Q: Is my API key safe?**  
A: Your key is stored only in the browser's memory for the session. It is never saved to disk, sent to any server other than Google, or logged anywhere.

**Q: Why doesn't it work when I open the HTML file directly?**  
A: Browsers block network requests from `file://` URLs as a security measure. Deploy to GitHub Pages or run a local server to fix this.

**Q: Can I change the AI model?**  
A: Yes! Replace `gemini-1.5-flash` with any model from [Google's model list](https://ai.google.dev/gemini-api/docs/models/gemini).
