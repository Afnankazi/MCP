# AI Chatbot (Gemini + WebSocket)

One-page React + Tailwind UI that talks to a single Node/Express + WebSocket backend powered by Google Gemini. Tools: generate code, detect bugs, check best practices, GitHub commit.

## Setup
1) Install deps  
```bash
npm install
```
2) Add `.env`  
```env
GEMINI_API_KEY=your_gemini_api_key
GITHUB_TOKEN=your_github_token   # needed for GitHub commits
PORT=3001                        # optional
```
3) Run  
```bash
npm start
```
Then open http://localhost:3001

## Project layout
```
server.js                      # Express + WebSocket + tool router
src/tools/                     # Gemini + GitHub tools
  generate-code.js
  detect-bugs.js
  check-best-practices.js
  github-commit.js
src/chatbot/web/               # React + Tailwind UI (served statically)
  index.html
  app.jsx
package.json
.env (local)
```

## Tips
- Type natural requests; use “help” to see tool hints.
- Paste code directly for bug/best-practice checks.
- For commits, provide repo, branch, path, and optional message.

