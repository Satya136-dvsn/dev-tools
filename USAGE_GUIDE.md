# 🚀 Universal AI Agent Environment: Usage Guide

Welcome to your high-performance, IDE-agnostic development environment. This guide will show you how to leverage your advanced tools to build better software faster while minimizing token costs.

---

## 🛠️ One-Time Setup (Already Done)
1. **Knowledge Graph**: `graphify` is installed and configured as an MCP server.
2. **Global Rules**: Token efficiency policies are active in `~/.agents/rules/`.
3. **Expert Roles**: The `MASTER_PROMPT.md` is ready for use.

---

## 🔄 Daily Workflow

Follow these 3 steps to start any coding task:

### Step 1: Initialize the Graph
Open your project folder in a terminal and run:
```bash
graphify extract ./
```
*This scans your project structure and creates a "map" that the AI uses to understand your code without reading every file.*

### Step 2: Activate the Expert Team
Open [MASTER_PROMPT.md](file:///C:/dev-tools/MASTER_PROMPT.md), copy the content, and paste it into your AI Coding Assistant (Cursor, Claude Code, Trae, Antigravity, etc.).

**Make sure to fill in these two fields:**
- `[FOLDER_PATH]`: The path to your project (e.g., `C:\VibeAnalytix`).
- `[YOUR_GOAL_HERE]`: What you want to accomplish.

### Step 3: Approve the Plan
The agent will enter a **Research & Discovery Phase**. It will map your architecture and present a plan. **Review this plan carefully** before giving the "Go" signal.

---

## 🧰 Key Tools & Capabilities

| Tool | Purpose | When to use |
| :--- | :--- | :--- |
| **Graphify** | Semantic mapping | For "How does X work?" or "Where is Y?" |
| **Code Review Graph** | Structural analysis | For "What will break if I change this?" |
| **Ruflo (Agentic Flow)** | Surgical editing | For applying code changes quickly and cheaply. |
| **Deep Research** | Web/Doc lookup | For researching new APIs or best practices. |

---

## ⚡ Power User: OpenClaude CLI

OpenClaude is your standalone terminal agent. It allows you to switch models (Gemini, DeepSeek, OpenAI) and manage MCP servers interactively.

### 1. Setup API Keys
You must set your API keys as environment variables. On Windows (PowerShell):
```powershell
[System.Environment]::SetEnvironmentVariable("GEMINI_API_KEY", "your_key", "User")
[System.Environment]::SetEnvironmentVariable("CLAUDE_CODE_USE_GEMINI", "1", "User")
```
*Restart your terminal after setting these.*

### 2. Launch OpenClaude
Navigate to your project folder and run:
```bash
openclaude
```

### 3. Key Commands inside OpenClaude
- `/provider`: Switch between Gemini, DeepSeek, or Anthropic.
- `/mcp`: Manage your Model Context Protocol servers (add Graphify here!).
- `/config`: See your active routing and model settings.
- `/compact`: Clear session history to save tokens.

---

## 🏔️ Free & Local: OpenClaude + Ollama

You can run your agents completely for free and offline using **Ollama**.

### 1. Start the Ollama Server
Ensure Ollama is running in your taskbar. If not, open a terminal and run:
```bash
ollama serve
```

### 2. Pull a Coding Model
We recommend **Qwen 2.5 Coder** for the best balance of speed and logic. Run this once:
```bash
ollama pull qwen2.5-coder:7b
```
*(Use `14b` or `32b` if you have a powerful GPU with 16GB+ VRAM).*

### 3. Connect OpenClaude to Ollama
1. Open your project folder.
2. Run `openclaude`.
3. Inside the chat, type:
```text
/provider ollama
/model qwen2.5-coder:7b
```

---

## 🏗️ Advanced Alternatives

If you need specific workflows beyond OpenClaude, consider these tools:

### 1. jcode (Coding Agent Harness)
A Rust-based tool designed for "Self-Dev" mode.
- **When to use**: If you want the agent to modify its own source code or run in a highly performance-optimized Rust environment.
- **Link**: [1jehuang/jcode](https://github.com/1jehuang/jcode)

### 2. free-claude-code (Backend Proxy)
A reverse proxy that allows you to use the official **Claude Code** CLI with local or alternative models.
- **When to use**: If you prefer the UX of the official `claude` command but want to route it to **Ollama**, **DeepSeek**, or **NVIDIA NIM**.
- **Link**: [Alishahryar1/free-claude-code](https://github.com/Alishahryar1/free-claude-code)


## 📉 Token Efficiency Tips
- **Be Surgical**: Don't ask the agent to "Refactor this whole folder." Ask for specific changes.
- **Use Checkpoints**: If a conversation goes over 20 messages, start a new one to clear the "context bloat."
- **Trust the Graph**: Let the agent use graph summaries instead of reading full source files.

---

## 🏁 Definition of Done
Every task you complete should pass the **Production Readiness Checklist** in the Master Prompt:
- [ ] **Security**: No secrets, valid inputs.
- [ ] **SEO/A11y**: Meta tags and ARIA labels checked.
- [ ] **Performance**: Optimized imports and renders.
- [ ] **Resiliency**: Error handling for all AI/External APIs.
- [ ] **Docs**: Updated README/Wiki.

---

*This environment is designed for professionals. Use it wisely to build elite-grade applications.*
