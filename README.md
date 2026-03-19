
# 🤖 AI PR Debugger (Local LLM)

An AI-powered GitHub Pull Request reviewer that automatically analyzes code changes and posts structured review comments — powered entirely by a **local LLM (Ollama + DeepSeek 6.7B)**.

 🚀 Features
* 🔍 Analyze GitHub PR diffs automatically
* 🧠 Detect bugs, issues, and improvements
* 💬 Post AI-generated comments directly on PRs
* ⚡ Runs locally (no paid API required)
* 🔐 Uses GitHub API for secure integration

 🏗️ Tech Stack
Backend: Node.js, Express
AI Model:DeepSeek Coder 6.7B (via Ollama)
APIs: GitHub REST API
HTTP Client: Axios

⚙️ How It Works

1. Fetches PR files using GitHub API
2. Extracts code diffs (`patch`)
3. Sends combined code to local LLM
4. AI generates structured review:

   * Issue
   * Root Cause
   * Fix
   * Corrected Code
5. Automatically posts review as a PR comment

📦 Setup

1. Clone repo

```bash
git clone https://github.com/icymalt28/ai-pr-debugger-demo.git
cd ai-pr-debugger-demo
```

2. Install dependencies

```bash
npm install
```

3. Setup environment

Create `.env` file:

```
GITHUB_TOKEN=your_github_token
```
 4. Run Ollama model

```bash
ollama run deepseek-coder:6.7b
```

 5. Start server

```bash
node server.js
```

 🧪 Usage

Trigger PR analysis:

```bash
 curl "http://127.0.0.1:3000/analyze-pr?owner=icymalt28&repo=ai-pr-debugger-demo&pr=1"
```

---

## 📸 Example Output

```
Issue: Variable used before declaration  
Root Cause: Missing initialization  
Fix: Define variable before usage  
Corrected Code:
let x = 10;
console.log(x);
```

---

## 🔥 Future Improvements

* 🔔 GitHub Webhooks (auto-trigger on PR open)
* 🧠 Smarter context-aware reviews
* 📍 Inline code comments (line-level feedback)
* 🌐 Frontend dashboard

---

💡 Why This Project?

Most AI code reviewers rely on paid APIs.
This project demonstrates how to build a **fully local, cost-free AI-powered developer tool**.

---


Built by **Kia Patil** 🚀

