# Coding Agents

## Table of Contents

1. **[GitHub Copilot](#github-copilot)**
2. **[OpenAI Codex](#openai-codex)**
3. **[Google](#google)**
4. **[Cursor](#cursor)**
5. **[Devin (Cognition AI)](#devin-cognition-ai)**
6. **[Windsurf](#windsurf)**
7. **[Kilo Code](#kilo-code)**
8. **[Replit](#replit)**
9. **[AWS](#aws)**
10. **[Cline](#cline)**
11. **[Augment Code](#augment-code)**
12. **[Amp Code (Sourcegraph)](#amp-code-sourcegraph)**
13. **[Roo Code](#roo-code)**
14. **[Continue](#continue)**
15. **[Tabnine](#tabnine)**
16. **[Zencoder](#zencoder)**
17. **[CodeGPT](#codegpt)**
18. **[Qodo (formerly Codium)](#qodo-formerly-codium)**
19. **[Junie](#junie)**
20. **[cto.new (Engine Labs)](#ctonew-engine-labs)**

---

## GitHub Copilot

[GitHub Copilot](https://github.com/features/copilot) is an AI-powered coding assistant developed by GitHub in collaboration with OpenAI. It helps developers write code faster by providing context-aware code suggestions, multi-line completions, and automated code edits, directly integrated into the IDE or command-line environment.

### Pricing

| Plan | Per Month (USD) | Per Year (USD) |
|------|------------------:|-----------------:|
| [Free](https://github.com/features/copilot/plans) | $0  | $0   |
| [Pro](https://github.com/features/copilot/plans)  | $10 | $100 |
| [Pro+](https://github.com/features/copilot/plans) | $39 | $390 |

### Offerings

**[VS Code agent mode](https://github.com/features/copilot/ai-code-editor):**
- **Type:** IDE extension
- **Where it runs:** Local machine (IDE) for file edits + cloud model API for reasoning.
- **Interaction:** Step‑by‑step interactive agent; you can clarify instructions mid‑task, accept/reject edits incrementally.
- **Scope:** Local repo in your IDE; multi‑file edits; human‑in‑the‑loop control.
- **Introduced:** [February 2025](https://code.visualstudio.com/blogs/2025/02/24/introducing-copilot-agent-mode)

**[Coding agent on GitHub](https://github.com/features/copilot/agents):**
- **Type:** Other (GitHub UI integration)
- **Where it runs:** GitHub‑hosted cloud runners (GitHub Actions).
- **Interaction:** Asynchronous agent; you assign a GitHub issue, it executes autonomously in the cloud, produces a draft PR, then you review.
- **Scope:** Full repo context; PR creation; works without you being present; no mid‑run intervention.
- **Introduced:** [September 2025](https://github.blog/changelog/2025-09-25-copilot-coding-agent-is-now-generally-available/)

**[Copilot CLI](https://github.com/features/copilot/cli):**
- **Type:** CLI tool
- **Where it runs:** Local machine (terminal) + cloud model API.
- **Interaction:** Command‑line interface for tasks; you provide instructions and the agent responds in the terminal.
- **Scope:** Flexible; can operate on local code, run scripts, generate snippets or refactors, or integrate with CI workflows.
- **Introduced:** [September 2025](https://github.blog/changelog/2025-09-25-github-copilot-cli-is-now-in-public-preview/)

**[Agent HQ](https://github.blog/news-insights/company-news/welcome-home-agents/):**
- **Type:** Other (centralized management platform)
- **Where it runs:** GitHub-hosted platform in the cloud.
- **Interaction:** Centralized hub for managing and monitoring all GitHub Copilot agents; provides overview dashboards and control interfaces.
- **Scope:** Organization-wide; integrates all Copilot agents and AI tools; enables governance, reporting, and management of agent activities.
- **Introduced:** [October 2025](https://github.blog/news-insights/company-news/welcome-home-agents/)

---

## OpenAI Codex

**[Codex Web (Cloud Agent)](https://openai.com/codex/):**
- **Type:** Web app (cloud-based)
- **Where it runs:** OpenAI cloud sandbox environments
- **Key features:** Asynchronous coding agent that can work on multiple tasks in parallel, each in isolated cloud sandbox

**[Codex CLI](https://github.com/openai/codex):**
- **Type:** CLI tool
- **Where it runs:** Local machine (terminal) + OpenAI API
- **Key features:** Open-source, runs locally, can read/modify/run code on your machine

**[Codex IDE Extension](https://help.openai.com/en/articles/11096431):**
- **Type:** IDE extension
- **Where it runs:** VS Code, Cursor, Windsurf
- **Key features:** Integrates with IDE, can delegate to cloud tasks or work locally

---

## Google

**[Jules](https://blog.google/technology/google-labs/jules/):**
- **Type:** Web app
- **Where it runs:** Google Cloud VMs
- **Key features:** Asynchronous coding agent, GitHub integration, works on full repositories

**[Gemini Code Assist](https://codeassist.google/):**
- **Type:** IDE extension
- **Where it runs:** Multiple IDEs (VS Code, JetBrains, Android Studio)
- **Key features:** Code completion, chat assistance, agent mode powered by Gemini 2.5

**[Firebase Studio](https://cloud.google.com/blog/products/ai-machine-learning/choose-the-right-google-ai-developer-tool-for-your-workflow):**
- **Type:** Web IDE
- **Where it runs:** Browser-based, Google-managed environment
- **Key features:** Full-stack app development, Gemini-powered, no-code/low-code approach

**[Gemini CLI](https://cloud.google.com/blog/products/ai-machine-learning/choose-the-right-google-ai-developer-tool-for-your-workflow):**
- **Type:** CLI tool
- **Where it runs:** Local terminal
- **Key features:** Lightweight CLI, MCP support, works with Gemini models

---

## Cursor

**[Cursor IDE](https://www.cursor.com/):**
- **Type:** Local IDE (VS Code fork)
- **Where it runs:** Local machine
- **Key features:** AI-first code editor with agent mode, codebase understanding, predictive editing

**[Cursor CLI](https://www.cursor.com/):**
- **Type:** CLI tool
- **Where it runs:** Local terminal
- **Key features:** Command-line agent for coding tasks

---

## Devin (Cognition AI)

**[Devin 2.0](https://devin.ai/):**
- **Type:** Web IDE (cloud-based)
- **Where it runs:** Cloud-based virtual machines
- **Key features:** Autonomous AI software engineer, parallel cloud agents, agent-native IDE experience

---

## Windsurf

**[Windsurf IDE](https://codeium.com/windsurf):**
- **Type:** Local IDE (VS Code fork)
- **Where it runs:** Local machine
- **Key features:** Agentic IDE with Cascade agent, flow tracking, multi-source context fusion

---

## Kilo Code

**[Kilo Code Extension](https://kilocode.ai/):**
- **Type:** IDE extension
- **Where it runs:** VS Code, JetBrains IDEs, Cursor, Windsurf
- **Key features:** Open-source AI coding assistant, multi-mode (Architect/Code/Debug), MCP marketplace, 400+ AI models

**[Kilo Code CLI](https://kilocode.ai/docs/cli):**
- **Type:** CLI tool
- **Where it runs:** Local terminal
- **Key features:** Terminal-based agent, autonomous mode for CI/CD, same engine as IDE extension

---

## Replit

**[Replit Agent](https://replit.com/):**
- **Type:** Web IDE
- **Where it runs:** Cloud-based development environment
- **Key features:** AI-powered development in browser, rapid prototyping, educational use

---

## AWS

**[Amazon Q Developer](https://aws.amazon.com/q/developer/):**
- **Type:** IDE extension
- **Where it runs:** Multiple IDEs (VS Code, JetBrains, Eclipse, Visual Studio)
- **Key features:** Code completion, chat assistance, AWS integration

**[Amazon Q Developer CLI](https://aws.amazon.com/q/developer/):**
- **Type:** CLI tool
- **Where it runs:** Local terminal
- **Key features:** Command-line interface to Q Developer capabilities

**[Kiro](https://kiro.dev/):**
- **Type:** Local IDE (VS Code fork)
- **Where it runs:** Local machine or cloud
- **Key features:** Specification-driven agentic IDE, autonomous agents with hooks, part of Amazon Q ecosystem

---

## Cline

**[Cline](https://github.com/cline/cline):**
- **Type:** IDE extension
- **Where it runs:** VS Code
- **Key features:** Open-source autonomous coding agent, file manipulation, terminal command execution

---

## Augment Code

**[Augment Code IDE Extension](https://www.augmentcode.com/):**
- **Type:** IDE extension
- **Where it runs:** Multiple IDEs
- **Key features:** AI coding assistant with codebase understanding

**[Auggie CLI](https://www.augmentcode.com/product/CLI):**
- **Type:** CLI tool
- **Where it runs:** Local terminal
- **Key features:** Command-line AI coding agent

---

## Amp Code (Sourcegraph)

**[Amp CLI](https://ampcode.com/):**
- **Type:** CLI tool
- **Where it runs:** Local terminal
- **Key features:** Terminal-based agentic coding, unconstrained token usage

**[Amp IDE Extension](https://sourcegraph.com/amp):**
- **Type:** IDE extension
- **Where it runs:** VS Code, Cursor, Windsurf
- **Key features:** Frontier coding agent, thread sharing, extended thinking mode

---

## Roo Code

**[Roo Code](https://roocode.com/):**
- **Type:** IDE extension
- **Where it runs:** VS Code
- **Key features:** Open-source, multiple specialized agent modes (Architect, Code, Debug), bring-your-own-model

---

## Continue

**[Continue IDE Extension](https://continue.dev/):**
- **Type:** IDE extension
- **Where it runs:** VS Code, JetBrains IDEs
- **Key features:** Open-source platform for creating custom AI assistants, supports local and remote models

**[Continue CLI](https://docs.continue.dev/cli/overview):**
- **Type:** CLI tool
- **Where it runs:** Local terminal
- **Key features:** Command-line interface for Continue, supports same models and customization as IDE extension

---

## Tabnine

**[Tabnine](https://www.tabnine.com/):**
- **Type:** IDE extension
- **Where it runs:** Multiple IDEs (VS Code, JetBrains, etc.)
- **Key features:** Privacy-focused AI code completion, can learn from your codebase, supports air-gapped deployment

---

## Zencoder

**[Zencoder](https://zencoder.ai/):**
- **Type:** IDE extension
- **Where it runs:** VS Code
- **Key features:** AI coding assistant with multimedia processing focus, repair agents for bug fixing

---

## CodeGPT

**[CodeGPT](https://codegpt.co/):**
- **Type:** IDE extension
- **Where it runs:** VS Code, JetBrains IDEs, Cursor
- **Key features:** Customizable AI agents, marketplace with 200+ specialized agents, supports custom model integration

---

## Qodo (formerly Codium)

**[Qodo](https://www.qodo.ai/):**
- **Type:** IDE extension
- **Where it runs:** VS Code, JetBrains IDEs
- **Key features:** Code integrity and testing focus, automated code review (Qodo Merge), test generation (Qodo Gen)

---

## Junie

**[Junie](https://www.jetbrains.com/):**
- **Type:** IDE extension
- **Where it runs:** JetBrains IDEs
- **Key features:** JetBrains' coding agent, deep IDE integration

---

## cto.new (Engine Labs)

**[cto.new](https://cto.new):**
- **Type:** Web app
- **Where it runs:** Cloud VMs (browser-based)
- **Key features:** AI coding platform with GitHub integration, executes code changes and opens PRs, planned free unlimited access to GPT-5, Claude Sonnet 4.5, and Gemini 2.5 Pro (ad-supported with data used for model training)
- **Status:** Not yet generally available (waitlist)