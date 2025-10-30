# CLI Coding Agents and Models Overview
**Last Updated: October 27, 2025**  
**Author: Daniel Weibel (weibeld)**

This document gives an overview of the most popular CLI coding agents and their compatibility with AI models across 5 major provider categories: OpenAI, Anthropic, Google, xAI (X), and Other providers. It focuses on those CLI coding agents that are compatible with [GitHub Spec Kit](https://github.com/github/spec-kit).

---

## Table of Contents

- **[1. Agent/Model Compatibility Matrix](#1-agentmodel-compatibility-matrix)**
- **[2. Agents](#2-agents)**
  - **[2.1. Gemini CLI (Google)](#21-gemini-cli-google)**
  - **[2.2. Codex CLI (OpenAI)](#22-codex-cli-openai)**
  - **[2.3. Claude Code (Anthropic)](#23-claude-code-anthropic)**
  - **[2.4. GitHub Copilot CLI (Microsoft/GitHub)](#24-github-copilot-cli-microsoftgithub)**
  - **[2.5. Amazon Q Developer CLI (AWS)](#25-amazon-q-developer-cli-aws)**
  - **[2.6. Cursor CLI (Cursor)](#26-cursor-cli-cursor)**
  - **[2.7. Aider (Paul Gauthier)](#27-aider-paul-gauthier)**
  - **[2.8. OpenCode (SST)](#28-opencode-sst)**
  - **[2.9. Goose (Block/Square)](#29-goose-blocksquare)**
  - **[2.10. Crush (Charm)](#210-crush-charm)**
  - **[2.11. Auggie CLI (Augment Code)](#211-auggie-cli-augment-code)**
  - **[2.12. Amp (Sourcegraph)](#212-amp-sourcegraph)**
  - **[2.13. Kilo Code (Kilo.org)](#213-kilo-code-kilo-org)**
  - **[2.14. Continue (Continue Dev)](#214-continue-continue-dev)**
- **[3. Models](#3-models)**
  - **[3.1. Google](#31-google)**
  - **[3.2. OpenAI](#32-openai)**
  - **[3.3. Anthropic](#33-anthropic)**
  - **[3.4. xAI](#34-xai)**
  - **[3.5. Other](#35-other)**
- **[4. Model Aggregators](#4-model-aggregators)**
  - **[4.1. OpenRouter](#41-openrouter)**
  - **[4.2. Models.dev](#42-modelsdev)**
  - **[4.3. Requesty](#43-requesty)**
  - **[4.4. Eden AI](#44-eden-ai)**
  - **[4.5. Portkey](#45-portkey)**
  - **[4.6. Hugging Face](#46-hugging-face)**
- **[5. Appendices](#5-appendices)**
  - **[5.1. Additional Coding Agents](#51-additional-coding-agents)**

---

## **1. Agent/Model Compatibility Matrix**

This matrix shows which AI models each CLI coding agent supports. We track 14 CLI agents across 5 model provider categories: **OpenAI**, **Anthropic**, **Google**, **xAI (X)**, and **Other** providers.

**Legend:**
- ✅ = Native support (direct API integration)
- 🔌 = Via aggregator (OpenRouter, etc.)
- ❌ = Not supported

---

| **Agent** | **[Google](#31-google)** | **[OpenAI](#32-openai)** | **[Anthropic](#33-anthropic)** | **[xAI (X)](#34-xai)** | **[Other](#35-other)** |
|-----------|------------|------------|---------------|-------------|-----------|
| **1. [Gemini CLI](#21-gemini-cli-google)** | ✅ Gemini 2.5 Pro (default), Gemini 2.5 Flash | ❌ | ❌ | ❌ | ❌ |
| **2. [Codex CLI](#22-codex-cli-openai)** | ❌ | ✅ o4-mini (default), GPT-4.1, GPT-5, o3, o4-mini | ❌ | ❌ | ❌ |
| **3. [Claude Code](#23-claude-code-anthropic)** | ❌ | ❌ | ✅ Claude Sonnet 4.5, Sonnet 4, Opus 4.1, Opus 4, Haiku 4.5, Haiku 3.5 | ❌ | ❌ |
| **4. [GitHub Copilot CLI](#24-github-copilot-cli-microsoftgithub)** | ✅ Gemini 2.5 Pro, 2.0 Flash | ✅ GPT-5, GPT-4.1 (default), GPT-5-Codex, GPT-5 Mini, o1, o3-mini | ✅ Claude Sonnet 4.5, Sonnet 4 (initial default), Opus 4.1, Haiku 4.5 | ✅ Grok Code Fast 1, Grok 3 (native xAI API + BYOK) | ✅ Via BYOK: Anthropic, OpenAI, Google, xAI, Azure, OpenRouter, Ollama, any OpenAI-compatible API |
| **5. [Amazon Q Developer CLI](#25-amazon-q-developer-cli-aws)** | ❌ | ❌ | ✅ Claude Sonnet 4.5, Sonnet 4 (default), Claude 3.7 Sonnet, Claude 3.5 Sonnet (via AWS Bedrock) | ❌ | ❌ |
| **6. [Cursor CLI](#26-cursor-cli-cursor)** | ✅ Gemini 2.5 Pro, 2.5 Flash, 2.0 Flash (managed + BYOK) | ✅ GPT-5, GPT-4.1, GPT-4o, GPT-4o Mini, o1, o3-mini (managed + BYOK) | ✅ Claude Sonnet 4.5, Sonnet 4, Opus 4.1, Opus 4, Claude 3.7 Sonnet, Haiku (managed + BYOK) | 🔌 Via OpenRouter (Grok 3, Grok 3 Mini, Grok Code Fast) | ✅ Via BYOK: Azure OpenAI, AWS Bedrock, any OpenAI-compatible API |
| **7. [Aider](#27-aider-paul-gauthier)** | ✅ Gemini 2.5 Pro, 2.5 Flash, 2.0 Flash | ✅ GPT-5, GPT-4o, GPT-4o Mini, o1, o3-mini | ✅ Claude 3.7 Sonnet, Sonnet 4, Opus 4, Haiku | 🔌 Via OpenRouter | ✅ Via LiteLLM: 200+ models, OpenRouter, Groq, Azure, Cohere, DeepSeek, Ollama local models |
| **8. [OpenCode](#28-opencode-sst)** | ✅ Gemini 2.5 Pro, 2.0 Flash, Pro | ✅ GPT-5, GPT-4o, o1 | ✅ Claude Sonnet 4.5, 4, Opus, Haiku | 🔌 Via OpenRouter | ✅ 75+ providers via Models.dev, Ollama local models, AWS Bedrock, Azure, Groq, DeepSeek |
| **9. [Goose](#29-goose-blocksquare)** | ✅ Gemini 2.5 Pro, 2.0 Flash, Pro | ✅ GPT-5, GPT-4o, o1 | ✅ Sonnet 4.5, 4, Opus, Haiku | ✅ Grok (via xAI API) | ✅ Llama (Groq/Ollama), AWS Bedrock, Mistral, 300+ via OpenRouter/Tetrate |
| **10. [Crush](#210-crush-charm)** | ✅ Gemini models (via Google AI API or VertexAI) | ✅ GPT models (via OpenAI API) | ✅ Claude models (via Anthropic API) | ✅ Grok (via xAI API) | ✅ Groq, AWS Bedrock, Azure |
| **11. [Auggie CLI](#211-auggie-cli-augment-code)** | ❌ | ✅ GPT-5 | ✅ Claude Sonnet 4.5 (default), Sonnet 4, Claude 3.7 Sonnet | ❌ | ❌ |
| **12. [Amp](#212-amp-sourcegraph)** | ❌ | ✅ GPT-5 (Oracle subagent for reasoning) | ✅ Claude Sonnet 4.5 (main agent, default) | ❌ | ❌ |
| **13. [Kilo Code](#213-kilo-code-kilo-org)** | ✅ Gemini 2.5 Pro, 2.0 Flash | ✅ GPT-5, GPT-4.1, GPT-4o, o1, o3-mini | ✅ Claude Sonnet 4.5, Sonnet 4, Opus 4.1, Opus 4, Claude 3.7 Sonnet, Haiku | 🔌 Via OpenRouter (Grok models) | ✅ 500+ models via 60+ providers (Kilo Gateway, OpenRouter, AWS Bedrock, Azure, Groq, DeepSeek, Mistral, Ollama local models) |
| **14. [Continue](#214-continue-continue-dev)** | ✅ Gemini 2.5 Pro, 2.0 Flash, Pro | ✅ GPT-5, GPT-4.1, GPT-4o, GPT-4o Mini, o1, o3-mini | ✅ Claude Sonnet 4.5, Sonnet 4, Opus 4, Haiku | 🔌 Via OpenRouter (Grok models) | ✅ Via LiteLLM: 200+ models, OpenRouter, AWS Bedrock, Azure, Groq, Cohere, DeepSeek, Mistral, Ollama local models, any OpenAI-compatible API |

---

## **2. Agents**

Overview of the CLI coding agents discussed in this document (click in table to jump to relevant section).

**Overview:**

| **Agent** | **GitHub Stars** | **Organisation** | **Open Source** | **Spec Kit Compatible** |
|-----------|------------------|------------------|-----------------|------------------------|
| **1. [Gemini CLI](#21-gemini-cli-google)** | ~80.5k | Google | ✅ Yes | ✅ Yes |
| **2. [Codex CLI](#22-codex-cli-openai)** | ~49k | OpenAI | ✅ Yes | ✅ Yes |
| **3. [Claude Code](#23-claude-code-anthropic)** | ~40.4k | Anthropic | ✅ Yes | ✅ Yes |
| **4. [GitHub Copilot CLI](#24-github-copilot-cli-microsoftgithub)** | ~4.1k | GitHub (Microsoft) | ✅ Yes | ✅ Yes |
| **5. [Amazon Q Developer CLI](#25-amazon-q-developer-cli-aws)** | N/A | Amazon Web Services | ❌ No | ✅ Yes |
| **6. [Cursor CLI](#26-cursor-cli-cursor)** | N/A | Cursor (Anysphere) | ❌ No | ✅ Yes |
| **7. [Aider](#27-aider-paul-gauthier)** | ~35k | Paul Gauthier (indie) | ✅ Yes | ❌ No ([Issue #1021](https://github.com/github/spec-kit/issues/1021)) |
| **8. [OpenCode](#28-opencode-sst)** | ~26k | SST (Serverless Stack) | ✅ Yes | ✅ Yes |
| **9. [Goose](#29-goose-blocksquare)** | ~20.6k | Block (formerly Square) | ✅ Yes | ❌ No ([PR #677](https://github.com/github/spec-kit/pull/677)) |
| **10. [Crush](#210-crush-charm)** | ~14.2k | Charm (Charmbracelet) | ✅ Yes | ❌ No ([Issue #396](https://github.com/github/spec-kit/issues/396)) |
| **11. [Auggie CLI](#211-auggie-cli-augment-code)** | ~50 | Augment Code | ✅ Yes | ✅ Yes |
| **12. [Amp](#212-amp-sourcegraph)** | N/A | Sourcegraph | ❌ No | ✅ Yes |
| **13. [Kilo Code](#213-kilo-code-kilo-org)** | ~11.6k | Kilo.org | ✅ Yes | ✅ Yes |
| **14. [Continue](#214-continue-continue-dev)** | ~29k | Continue Dev, Inc. | ✅ Yes | ❌ No ([Issue #1489](https://github.com/continuedev/continue/issues/1489)) |

---
### **2.1. Gemini CLI** (Google)
- **Organisation:** [Google](https://ai.google.dev)
- **Website:** https://ai.google.dev
- **GitHub:** https://github.com/google-gemini/gemini-cli (⭐ ~80.5k)
- **Project Context:** Component of Google's Gemini suite including [Gemini Code Assist](https://cloud.google.com/gemini/docs/codeassist/overview) for IDEs, [Gemini Canvas](https://gemini.google.com/canvas) for web, and [Jules](https://ai.google.dev/gemini-api/docs/jules) for autonomous coding
- **Model Access:** Direct API integration with Google AI API. Exclusively supports Gemini models.
- **Description:** Google's official open-source (Apache 2.0) CLI agent released June 2025. Brings Gemini 2.5 Pro directly to terminal with built-in tools (Google Search grounding, file operations, shell commands, web fetching). MCP (Model Context Protocol) support for custom extensions.
- **Pricing:** Free tier with 60 requests/min, 1,000 requests/day, 1M context window. [Pricing details](https://ai.google.dev/pricing)
- **Notable:** Highest-starred agent in matrix (~80.5k). Does NOT support non-Google models natively - Google team states they are "optimizing Gemini CLI for Gemini models, and not building direct support for other LLM providers." Community forks exist with multi-provider support but are not officially maintained.
- **Spec Kit Compatibility:** ✅

[⬆️ Up](#2-agents)

---

### **2.2. Codex CLI** (OpenAI)
- **Organisation:** [OpenAI](https://openai.com)
- **Website:** https://platform.openai.com
- **GitHub:** https://github.com/openai/codex (⭐ ~49k)
- **Project Context:** Component of OpenAI's coding tools ecosystem alongside [Codex in ChatGPT](https://openai.com/chatgpt)
- **Model Access:** Direct API integration with OpenAI API. Exclusively supports OpenAI models.
- **Description:** OpenAI's official CLI tool for AI-powered coding directly in your terminal. Released alongside o3/o4-mini models in April 2025. Open-source under Apache 2.0 license. Experimental project under active development with community contributions welcome. Chat-driven development that can read files, write files via patches, and execute shell commands in sandboxed environment. Multimodal support (text, screenshots, diagrams).
- **Pricing:** Free CLI tool, pay OpenAI API costs. Medium-sized code changes typically cost $3-4 with o3 model. OpenAI offers $1M API grants initiative for open-source Codex CLI projects. [API pricing](https://openai.com/api/pricing/)
- **Spec Kit Compatibility:** ✅

[⬆️ Up](#2-agents)

---

### **2.3. Claude Code** (Anthropic)
- **Organisation:** [Anthropic](https://anthropic.com)
- **Website:** https://claude.ai
- **GitHub:** https://github.com/anthropics/claude-code (⭐ ~40.4k)
- **Project Context:** Component of Anthropic's Claude ecosystem including [Claude.ai](https://claude.ai) web, [Claude API](https://docs.anthropic.com), and [Claude in IDEs](https://www.anthropic.com/news/claude-code)
- **Model Access:** Direct API integration with Anthropic API. Exclusively supports Claude models via Claude Pro/Max subscription or API key.
- **Description:** Anthropic's official CLI tool for Claude-powered coding assistance. Terminal-native agent with autonomous capabilities, MCP (Model Context Protocol) support, and deep codebase understanding. Generally available since May 2025. Opus Plan Mode automatically switches between Opus 4.1 (planning/research) and Sonnet 4.5 (implementation).
- **Pricing:** Claude Pro ($20/month), Claude Max, or Anthropic API key. API pricing: Sonnet 4.5 at $3/$15 per million tokens, Opus 4.1 at $15/$75 per million tokens, Haiku 4.5 at $1/$5 per million tokens. [Pricing details](https://www.anthropic.com/pricing)
- **Spec Kit Compatibility:** ✅

[⬆️ Up](#2-agents)

---

### **2.4. GitHub Copilot CLI** (Microsoft/GitHub)
- **Organisation:** [GitHub](https://github.com) (Microsoft)
- **Website:** https://github.com/features/copilot
- **GitHub:** https://github.com/github/copilot-cli (⭐ ~4.1k)
- **Project Context:** Component of GitHub Copilot platform including [IDE extensions](https://github.com/features/copilot), [Copilot Chat](https://docs.github.com/en/copilot/using-github-copilot/asking-github-copilot-questions-in-your-ide), [Copilot Coding Agent](https://github.blog/news-insights/product-news/github-copilot-meet-the-new-coding-agent/)
- **Model Access:** Managed by GitHub Models backend (native support for OpenAI, Anthropic, Google, xAI) or bring your own API keys for any provider.
- **Description:** Terminal-native coding agent that brings GitHub Copilot directly to command line. Part of broader GitHub Copilot ecosystem (IDE extensions, Copilot Chat, Copilot Coding Agent). Supports MCP (Model Context Protocol) for extensibility. Works against GitHub Models backend with orchestrated routing. Can switch models during session without losing context using `/model` slash command. BYOK supports Anthropic, OpenAI, Google, xAI, Azure, OpenRouter, Ollama, and any OpenAI-compatible API.
- **Pricing:** Included with GitHub Copilot subscription: Individual ($10/month), Business ($19/user/month), Enterprise ($39/user/month). No separate API keys needed. [Pricing details](https://github.com/features/copilot/plans)
- **Spec Kit Compatibility:** ✅

[⬆️ Up](#2-agents)

---

### **2.5. Amazon Q Developer CLI** (AWS)
- **Organisation:** [Amazon Web Services](https://aws.amazon.com)
- **Website:** https://aws.amazon.com/q/developer/
- **GitHub:** ❌ Not open-source (proprietary)
- **Project Context:** Component of Amazon Q Developer platform including [IDE extensions](https://aws.amazon.com/q/developer/), [inline suggestions](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/inline-suggestions.html), [Q Chat](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/chat.html), [AWS integration](https://aws.amazon.com/q/developer/resources/)
- **Model Access:** AWS Bedrock managed service - Exclusively supports Anthropic Claude models. AWS manages model access.
- **Description:** AWS's AI coding assistant with CLI interface launched March 2025. Part of broader Amazon Q ecosystem integrated with AWS services. Powered by Amazon Bedrock with advanced agentic capabilities. Supports conversation persistence, MCP (Model Context Protocol), image support, context management, and git-aware file selection. Latest version (v1.11.0+) includes Claude Sonnet 4.5 support at no additional cost. Requires AWS authentication (Builder ID or AWS account).
- **Pricing:** Free tier with AWS Builder ID (no AWS account required), Pro at $19/month (1,000 requests), Pro+ at $39/month (3,000 requests). Can use AWS credits (e.g., AWS Community Builder $500/year credits). [Pricing details](https://aws.amazon.com/q/developer/pricing/)
- **Notable:** Deep integration with AWS Bedrock and AWS development workflows. Excels when working with AWS resources (DynamoDB, S3, etc.). Model selection limited to Anthropic Claude family - no multi-provider support.
- **Spec Kit Compatibility:** ✅

[⬆️ Up](#2-agents)

---

### **2.6. Cursor CLI** (Cursor)
- **Organisation:** [Cursor](https://cursor.com) (Anysphere)
- **Website:** https://cursor.com
- **GitHub:** ❌ Not open-source (proprietary)
- **Project Context:** Component of Cursor IDE ecosystem (forked from VS Code)
- **Model Access:** Hybrid - Managed via Cursor subscription OR bring your own API keys for OpenAI, Anthropic, Google, Azure, AWS Bedrock, OpenRouter, and OpenAI-compatible APIs.
- **Description:** Command-line interface for Cursor's AI-powered IDE. Released in beta August 2025. Part of the larger Cursor ecosystem (forked from VS Code). Works across any IDE or terminal environment - VS Code, JetBrains, Android Studio, Neovim, etc. Supports MCP (Model Context Protocol) for extensibility. xAI Grok models accessible via OpenRouter integration. Automatic model selection with "Auto" mode. Can detect model issues and switch automatically. Supports both interactive and non-interactive (CI/CD) modes.
- **Pricing:** Free tier, Pro ($20/month), Pro Plus, Ultra ($200/month). BYOK option available to use your own API keys instead of subscription. [Pricing details](https://cursor.com/pricing)
- **Notable:** Most flexible pricing model among CLI agents - choose between managed subscription (no API keys needed) or BYOK (bring your own keys). Security safeguards still evolving (beta status).
- **Spec Kit Compatibility:** ✅

[⬆️ Up](#2-agents)

---

### **2.7. Aider** (Paul Gauthier)
- **Organisation:** [Paul Gauthier](https://github.com/paul-gauthier) (individual developer)
- **Website:** https://aider.chat
- **GitHub:** https://github.com/paul-gauthier/aider (⭐ ~35k)
- **Project Context:** Standalone project
- **Model Access:** Direct API with OpenAI, Anthropic, Google + OpenRouter (200+ models) + Local models via Ollama. Bring your own API keys.
- **Description:** Independent, terminal-only AI pair programmer with git-first workflow. Free open-source tool, pay your own API costs. Supports multiple edit formats for various LLMs. Context management with smart file selection and repository map for semantic codebase understanding. Via LiteLLM package connects to Azure, Groq, Cohere, DeepSeek, and any OpenAI-compatible API. Git integration automatically commits changes with descriptive messages (can be disabled).
- **Pricing:** Free open-source tool. Pay your own API costs for whichever model provider you choose. [Model pricing varies by provider]
- **Notable:** Strong SWE-bench performance.
- **Spec Kit Compatibility:** ❌ [github/spec-kit Issue #1021](https://github.com/github/spec-kit/issues/1021)

[⬆️ Up](#2-agents)

---

### **2.8. OpenCode** (SST)
- **Organisation:** [SST](https://sst.dev) (Serverless Stack)
- **Website:** https://opencode.ai
- **GitHub:** https://github.com/sst/opencode (⭐ ~26k)
- **Project Context:** Standalone project
- **Model Access:** Direct API with 75+ providers via Models.dev (SST's model aggregator) + OpenRouter + Local models via Ollama. Bring your own API keys or use Claude Pro/Max subscription.
- **Description:** Terminal-first AI coding agent built by SST team (creators of terminal.shop). Model-agnostic with 75+ provider support via Models.dev (SST's own model aggregator) and OpenRouter, including OpenAI, Anthropic, Google, AWS Bedrock, Azure, DeepSeek, Groq, Mistral, xAI. Free open-source (MIT license). LSP integration for code intelligence. Multiple parallel agent sessions. Session management and persistence (SQLite). Vim-like integrated editor. Non-interactive mode for scripting. Terminal User Interface (TUI) built with Bubble Tea. Does NOT store code or context - runs locally.
- **Pricing:** Free open-source tool (MIT license). Pay your own API costs or use Claude Pro/Max subscription. OpenCode Zen offers curated, benchmarked models with transparent pricing.
- **Spec Kit Compatibility:** ✅

[⬆️ Up](#2-agents)

---

### **2.9. Goose** (Block/Square)
- **Organisation:** [Block](https://block.xyz) (formerly Square)
- **Website:** https://block.github.io/goose
- **GitHub:** https://github.com/block/goose (⭐ ~20.6k)
- **Project Context:** Standalone project with both desktop app and CLI
- **Model Access:** Direct API with OpenAI, Anthropic, Google, xAI, AWS Bedrock + OpenRouter/Tetrate (300+ models) + Local models via Ollama. Bring your own API keys.
- **Description:** Block's AI agent for coding and workflow automation. Supports both GUI desktop app (macOS, Windows) and CLI interface. MCP protocol for enterprise integrations. Works with any LLM that supports tool calling. Can automate tasks across Slack, Jira, GitHub, DynamoDB, etc. Runs locally on your machine for privacy.
- **Pricing:** Free framework (Apache 2.0), pay for LLM provider of choice. Tetrate Agent Router offers $10 free credits when authenticating through Goose.
- **Notable:** Broader scope than just coding - automates tasks across multiple systems.
- **Spec Kit Compatibility:** ❌ [github/spec-kit PR #677](https://github.com/github/spec-kit/pull/677)

[⬆️ Up](#2-agents)

---

### **2.10. Crush** (Charm)
- **Organisation:** [Charm](https://charm.land)
- **Website:** https://charm.sh/crush
- **GitHub:** https://github.com/charmbracelet/crush (⭐ ~14.2k)
- **Project Context:** Standalone project
- **Model Access:** Direct API with OpenAI, Anthropic, Google, xAI, Groq, AWS Bedrock, Azure + OpenRouter (300+ models) + Any OpenAI/Anthropic-compatible API including local models. Bring your own API keys.
- **Description:** Terminal AI coding agent from Charm, makers of popular terminal tools (Glow, VHS, Bubble Tea). Beautiful TUI with LSP integration and MCP support. Built with Go using Bubble Tea framework. Written in Go (single binary). Cross-platform: macOS, Linux, Windows, FreeBSD, OpenBSD, NetBSD. Models managed via Catwalk community database with automatic updates. Zero config - works out of box with sensible defaults. Supports mid-session model switching without losing context.
- **Pricing:** Free open-source tool. Pay your own API keys. Model listings automatically update from Catwalk community database.
- **Notable:** Collects pseudonymous usage metrics (opt-out available), but prompts/responses NEVER collected.
- **Spec Kit Compatibility:** ❌ [github/spec-kit Issue #396](https://github.com/github/spec-kit/issues/396)

[⬆️ Up](#2-agents)

---

### **2.11. Auggie CLI** (Augment Code)
- **Organisation:** [Augment Code](https://augmentcode.com)
- **Website:** https://augmentcode.com
- **GitHub:** https://github.com/augmentcode/auggie (⭐ ~50)
- **Project Context:** Component of Augment Code platform
- **Model Access:** Managed by Augment - Fixed model selection (Claude Sonnet 4.5, GPT-5). Users cannot bring own API keys.
- **Description:** Augment Code's agentic CLI tool launched August 2025 in private beta. Built for enterprise teams with $252M in funding. Proprietary context engine provides deep codebase understanding with real-time indexing, code structure awareness, and 10,000 commit history. Unix-style tool design for script integration. Supports both interactive and non-interactive modes. Compatible with Claude Code's slash command interface (detects .claude/commands/ directory). Built-in integrations with CircleCI, MongoDB, Redis, Sentry, Stripe.
- **Pricing:** Developer tier at $50/month (~600 messages/month). Users pay Augment, not model providers directly. [Pricing details](https://augmentcode.com/pricing)
- **Notable:** Does NOT support user-supplied API keys - fully managed service model. Token-efficient due to selective retrieval vs context dumping.
- **Spec Kit Compatibility:** ✅

[⬆️ Up](#2-agents)

---

### **2.12. Amp** (Sourcegraph)
- **Organisation:** [Sourcegraph](https://sourcegraph.com)
- **Website:** https://sourcegraph.com/amp
- **GitHub:** ❌ Not open-source (proprietary)
- **Project Context:** Component of Sourcegraph's AI coding suite (includes both CLI and IDE extensions)
- **Model Access:** Managed by Sourcegraph - Multi-model architecture with Claude Sonnet 4.5 (main agent) and GPT-5 (Oracle reasoning subagent). Users cannot choose models or bring own API keys.
- **Description:** Professional AI coding agent built by Sourcegraph with both CLI and IDE support. Launched as "Research Preview" in 2025. Engineered to maximize frontier model capabilities through multi-model orchestration. System automatically routes between Sonnet 4.5 (main work) and GPT-5 (reasoning) based on task complexity or explicit user request to "use the oracle". Also includes Librarian subagent for cross-repository codebase search. Supports MCP (Model Context Protocol), AGENTS.md configuration files, thread system (like Git branches for conversations), and collaborative features (shared workspaces, thread linking). Spec Kit compatible. Unconstrained token usage - no artificial limits.
- **Pricing:** Amp Free ($0/month, ad-supported) or Amp Smart (prepaid credits, ~$5-15 per PR typical). [Pricing details](https://sourcegraph.com/amp/pricing)
- **Notable:** Unique multi-model architecture - uses Claude Sonnet 4.5 as "Worker" and GPT-5 as "Oracle" for strategic reasoning. Amp Free tier is ad-supported and automatically selects models - users cannot bring own API keys or choose models. Built by team that created Sourcegraph code search.
- **Spec Kit Compatibility:** ✅

[⬆️ Up](#2-agents)

---

### **2.13. Kilo Code** (Kilo.org)
- **Organisation:** [Kilo.org](https://kilocode.ai)
- **Website:** https://kilocode.ai
- **GitHub:** https://github.com/Kilo-Org/kilocode (⭐ ~11.6k)
- **Project Context:** Standalone project with both CLI and IDE extensions (VS Code, JetBrains)
- **Model Access:** Hybrid - Built-in Kilo Gateway (500+ models via 60+ providers) OR bring your own API keys for direct provider access. Supports OpenAI, Anthropic, Google, xAI (via OpenRouter), AWS Bedrock, Azure, Groq, DeepSeek, Mistral, and any OpenAI-compatible API including Ollama local models.
- **Description:** Open-source AI coding assistant (Apache 2.0) launched March 2025. Evolved from merging best features of Cline and Roo Code. CLI interface released alongside VS Code and JetBrains extensions. Multi-mode system: Architect (planning), Code (implementation), Debug (systematic diagnosis), Ask (Q&A), Orchestrator (multi-agent coordination), plus custom modes. MCP (Model Context Protocol) support with marketplace for custom tools. Autonomous mode for CI/CD pipelines with configurable auto-approval. Terminal User Interface with keyboard-first navigation. Context-aware with LSP integration. Transparent about model usage - no silent model switching or context compression.
- **Pricing:** Free open-source tool. Pay via Kilo Gateway (matches provider list prices, no markup) or use your own API keys. New users get $20 bonus credits on first top-up. Also offers Teams (centralized billing, project analytics, role-based permissions) and Enterprise (SSO, SCIM, SLA, audit logs) tiers. [Pricing details](https://kilocode.ai/pricing)
- **Notable:** Kilo Gateway provides unified access to 500+ models from 60+ providers with no commission or hidden fees - transparent pricing matching Anthropic, OpenAI, and Google list prices exactly. Strong focus on transparency: users always see which model is being used, full context window size per request, and can view/modify all prompts. Built on shoulders of Cline and Roo Code with continuous integration of their improvements. Processes over 40 billion tokens daily through Kilo Gateway.
- **Spec Kit Compatibility:** ✅

[⬆️ Up](#2-agents)

---

### **2.14. Continue** (Continue Dev)
- **Organisation:** [Continue Dev, Inc.](https://continue.dev)
- **Website:** https://continue.dev
- **GitHub:** https://github.com/continuedev/continue (⭐ ~29k)
- **Project Context:** Standalone project with IDE extensions (VS Code, JetBrains) and CLI interface
- **Model Access:** Bring your own API keys for any LLM provider. Supports direct API integration with OpenAI, Anthropic, Google + via LiteLLM for 200+ models. Optional Continue Hub for managed API access and team configurations.
- **Description:** Open-source AI coding assistant (Apache 2.0) launched as Y Combinator startup (W23). Positioned as "open-source autopilot for software development" with deep customizability. CLI interface (`cn`) launched alongside IDE extensions with two distinct modes: TUI Mode (interactive development, exploration, debugging) and Headless Mode (production automation for CI/CD). Supports @ for context (files, URLs), / for slash commands, and full MCP (Model Context Protocol) support. Context-aware with same context providers as IDE extensions. Automatically collects development data locally (`.continue/dev_data`) for continuous learning. Works with any LLM including local models via Ollama. Integrated with Continue Hub for API access, secrets management, and configuration sync across teams.
- **Pricing:** Free open-source tool (Apache 2.0). Pay your own API costs for models OR use Continue Hub: Solo ($0), Teams ($10/developer/month with centralized management + $20 models add-on), Enterprise (custom pricing with SSO/SAML). [Pricing details](https://hub.continue.dev/pricing)
- **Notable:** One of the highest-starred coding agents (~29k stars). Y Combinator backed (W23). Built around philosophy of developer data ownership - collects development data locally that can be used to improve team-specific LLMs. Designed to be "continuously learning" from how you build software. Strong focus on customization and avoiding vendor lock-in. Supports both managed (Continue Hub) and fully self-hosted deployment options. LiteLLM integration provides unified interface to 200+ models.
- **Spec Kit Compatibility:** ❌ [github/spec-kit Issue #1489](https://github.com/continuedev/continue/issues/1489)

[⬆️ Up](#2-agents)

---

## **3. Models**

Descriptions of the AI models used in this document (click in table to jump to relevant section).

**Overview:**

| Category | Model | Input (USD/1M Tokens) | Output (USD/1M Tokens) | Context Size (Tokens) |
|----------|-------|----------------------:|----------------------:|--------------------:|
| **[Google](#31-google)**<br>([👉 Pricing](https://ai.google.dev/pricing)) | Gemini 3 | TBD | TBD | TBD |
| | Gemini 2.5 Pro (≤200K tokens) | $1.25 | $10.00 | 1M–2M |
| | Gemini 2.5 Pro (>200K tokens) | $2.50 | $15.00 | 1M–2M |
| | Gemini 2.5 Flash | $0.075 | $0.30 | 1M |
| | Gemini 2.0 Flash | $0.10 | $0.40 | 1M |
| | Gemini Pro | $1.25 | $5.00 | 2M |
| **[OpenAI](#32-openai)**<br>([👉 Pricing](https://openai.com/api/pricing/)) | GPT-5 | $1.25 | $10.00 | 128K |
| | GPT-5 Mini | $0.25 | $2.00 | 128K |
| | GPT-5 Nano | $0.05 | $0.40 | 128K |
| | GPT-4.1 | $2.50 | $10.00 | 128K |
| | GPT-4o | $2.50 | $10.00 | 128K |
| | GPT-4o Mini | $0.15 | $0.60 | 128K |
| | o1 | $15.00 | $60.00 | 200K |
| | o3 (Flex) | $1.00 | $4.00 | 200K |
| | o3 (Standard) | $15.00 | $60.00 | 200K |
| | o3-mini | $1.10 | $4.40 | 200K |
| | o4-mini | $1.10 | $4.40 | 200K |
| **[Anthropic](#33-anthropic)**<br>([👉 Pricing](https://www.anthropic.com/pricing)) | Claude Sonnet 4.5 | $3.00 | $15.00 | 200K |
| | Claude Sonnet 4 | $3.00 | $15.00 | 200K |
| | Claude 3.7 Sonnet | $3.00 | $15.00 | 200K |
| | Claude Opus 4.1 | $15.00 | $75.00 | 200K |
| | Claude Opus 4 | $15.00 | $75.00 | 200K |
| | Claude Haiku 4.5 | $1.00 | $5.00 | 200K |
| | Claude Haiku 3.5 | $0.80 | $4.00 | 200K |
| | Claude Haiku 3 | $0.25 | $1.25 | 200K |
| **[xAI](#34-xai)**<br>([👉 Pricing](https://docs.x.ai/docs/models)) | Grok 4 | $3.00 | $15.00 | 1M |
| | Grok 4 (cached) | $0.75 | $15.00 | 1M |
| | Grok 4 Fast (≤128K tokens) | $0.20 | $0.50 | 128K |
| | Grok 4 Fast (>128K tokens) | $0.40 | $1.00 | 1M |
| | Grok 4 Fast (cached) | $0.05 | — | 1M |
| | Grok Code Fast 1 | $0.20 | $0.50 | 128K |
| | Grok 3 | $3.00 | $15.00 | 1M |
| **[Mistral](#35-other)**<br>([👉 Pricing](https://mistral.ai/pricing)) | Mistral Large | $2.00 | $6.00 | 128K |
| | Mistral Medium 3 | $0.40 | $2.00 | 128K |
| | Mistral Small | $0.60 | $1.80 | 128K |
| **[DeepSeek](#35-other)**<br>([👉 Pricing](https://api-docs.deepseek.com/quick_start/pricing)) | DeepSeek Chat (cache hit) | $0.07 | $1.10 | 128K |
| | DeepSeek Chat (cache miss) | $0.27 | $1.10 | 128K |
| | DeepSeek Reasoner (cache hit) | $0.14 | $2.19 | 128K |
| | DeepSeek Reasoner (cache miss) | $0.55 | $2.19 | 128K |
| | DeepSeek V3.2 (cache hit) | $0.014 | $0.28 | 128K |
| | DeepSeek V3.2 (cache miss) | $0.14 | $0.28 | 128K |
| **[Meta](#35-other)**<br>(🤑 free for self-hosting) | Llama 3.3 70B (hosted by [OpenRouter](https://openrouter.ai/)) | $0.12 | $0.30 | 128K |

**Note:** Meta Llama models are open-source and free to download and self-host. For managed API access, pricing varies by third-party provider (AWS Bedrock, Google Vertex AI, Together.ai, Groq, etc.). Check individual provider pricing pages for costs.

---

### **3.1. Google**

#### **Gemini 3**
Google's next-generation flagship model expected in November 2025. Pricing not yet announced.

#### **Gemini 2.5 Pro**
Google's latest premium model with 2M token context window. Available free in experimental tier (rate limited).

#### **Gemini 2.5 Flash**
Ultra-fast, cost-effective model at $0.075 input / $0.30 output per 1M tokens with 1M context window.

#### **Gemini 2.0 Flash / 2.0 Flash Pro**
Current generation fast models balancing speed and performance at extremely competitive pricing.

#### **Gemini Pro**
Standard Gemini model with 2M context at $1.25 input / $5.00 output per 1M tokens, excellent for long-context tasks.

[⬆️ Up](#3-models)

---

### **3.2. OpenAI**

#### **GPT-5**
OpenAI's latest flagship model with advanced reasoning capabilities, multimodal support, and improved code generation. Estimated at $2.50 input / $10.00 output per 1M tokens.

#### **GPT-4.1**
Enhanced version of GPT-4 with improved performance and reliability. Used as default in GitHub Copilot CLI.

#### **GPT-4o / GPT-4o Mini**
GPT-4 Optimized models balancing performance and cost. Mini variant offers budget-friendly alternative at $0.15 input / $0.60 output per 1M tokens.

#### **o1 / o3 / o3-mini / o4-mini**
OpenAI's reasoning models optimized for complex problem-solving, mathematics, and algorithm design. o1 priced at $15 input / $60 output per 1M tokens.

#### **GPT-5-Codex**
Specialized variant of GPT-5 optimized specifically for code generation and programming tasks.

[⬆️ Up](#3-models)

---

### **3.3. Anthropic**

#### **Claude Sonnet 4.5**
Anthropic's latest and most advanced model, best-in-class for coding tasks. Priced at $3 input / $15 output per 1M tokens with 200K context window.

#### **Claude Sonnet 4**
Previous generation Sonnet model, still excellent for most coding tasks with same pricing as 4.5.

#### **Claude 3.7 Sonnet**
Earlier Sonnet version available in some agents, represents mid-2024 generation Claude capabilities.

#### **Claude Opus 4.1 / Opus 4**
Claude's most powerful models for complex reasoning tasks. Priced at $15 input / $75 output per 1M tokens.

#### **Claude Haiku 4.5 / Haiku 3.5**
Fast, cost-effective Claude models for routine tasks. Haiku 4.5 at $1 input / $5 output per 1M tokens.

[⬆️ Up](#3-models)

---

### **3.4. xAI**

#### **Grok / Grok 3 / Grok 3 Mini**
xAI's flagship models known for uncensored outputs and alternative perspectives. Accessible via native xAI API or OpenRouter.

#### **Grok Code Fast / Grok Code Fast 1**
Specialized Grok variants optimized for fast code generation and programming assistance.

#### **Grok 4 / Grok 4 Fast**
Latest generation models with advanced reasoning capabilities and unified architecture supporting 2M token context window.

[⬆️ Up](#3-models)

---

### **3.5. Other**

#### **Llama Models (Meta)**
Open-source models from Meta including Llama 3.1 (405B) and Llama 4 variants. Free to download and self-host. No direct Meta API - access through third-party providers (AWS Bedrock, Google Vertex AI, Together.ai, Groq, etc.) with their own pricing, or self-host for free.

#### **Mistral Models**
European AI alternatives with strong code generation capabilities. Direct API access through Mistral's "la Plateforme" with competitive pricing.

#### **DeepSeek Models**
Chinese AI models with exceptional cost-efficiency and performance. Direct API access through DeepSeek with industry-leading low pricing.

[⬆️ Up](#3-models)

---

## **4. Model Aggregators**

Third-party platforms providing unified access to multiple AI models through a single API, eliminating the need to manage separate API keys for each provider.

---

### **4.1. OpenRouter**
**Website:** [openrouter.ai](https://openrouter.ai)

- OpenRouter is a unified API gateway providing access to 300+ AI models from various providers through a single API key.
- Offers transparent pricing with no markup on model costs, plus automatic failover and smart load balancing.
- Many models available completely free (Llama 4, Gemini 2.5 Pro Experimental, etc.).
- Seamless integration with most coding agents.

**Best for:** Developers wanting to access multiple models without juggling API keys, trying free models, and seamless integration with most coding agents.

[⬆️ Up](#table-of-contents)

---

### **4.2. Models.dev**
**Website:** [models.dev](https://models.dev)

- Models.dev is SST's model aggregation platform providing unified access to 75+ AI model providers through a single API.
- Built originally for OpenCode but available for any coding agent or application to use.
- OpenAI-compatible API format for easy integration with existing tools.
- Transparent pricing with pay-as-you-go model across all supported providers.
- Supports major providers: OpenAI, Anthropic, Google, AWS Bedrock, Azure, DeepSeek, Groq, Mistral, xAI, and more.

**Best for:** Developers wanting SST's curated model selection, teams already using OpenCode, and projects needing OpenAI-compatible API for 75+ providers.

[⬆️ Up](#table-of-contents)

---

### **4.3. Requesty**
**Website:** [requesty.ai](https://www.requesty.ai)

- Requesty is an intelligent routing platform that automatically classifies tasks and routes them to optimal models for cost efficiency.
- Offers 30-80% cost savings by routing simple requests to cheaper models and complex tasks to premium models.
- OpenRouter API compatible with built-in budget thresholds, usage caps, and advanced guardrails.
- Includes comprehensive analytics and monitoring tools.

**Best for:** Enterprises needing automatic cost optimization and advanced analytics without manual model selection.

[⬆️ Up](#table-of-contents)

---

### **4.4. Eden AI**
**Website:** [edenai.co](https://www.edenai.co)

- Eden AI provides a single API for accessing top LLMs plus additional AI services like image generation, translation, and text-to-speech.
- Features pay-as-you-go pricing with automatic selection of the cheapest model for each task.
- Enterprise-grade scalability with support for multi-modal AI capabilities.
- Unified billing across all AI providers and services.

**Best for:** Projects requiring diverse AI capabilities beyond text generation, teams wanting multi-modal AI services through one unified API.

[⬆️ Up](#table-of-contents)

---

### **4.5. Portkey**
**Website:** [portkey.ai](https://portkey.ai)

- Portkey is a comprehensive AI control panel offering smart routing, caching, and monitoring for AI applications.
- Provides unified interface to 250+ AI models with automatic model selection based on task requirements.
- Built-in caching and rate limiting to optimize costs and performance.
- Comprehensive observability tools with detailed logs, metrics tracking, and real-time monitoring.
- Free tier available with 10k requests per month; open-source gateway option.

**Best for:** Teams needing detailed observability, optimization, and governance over their AI model usage.

[⬆️ Up](#table-of-contents)

---

### **4.6. Hugging Face**
**Website:** [huggingface.co](https://huggingface.co)

- Hugging Face is a comprehensive model hub providing access to thousands of open-source AI models.
- Three access methods: Inference API (pay-per-use hosted), Inference Endpoints (dedicated instances at ~$0.60/hour), and Model Downloads (free self-hosted).
- OpenAI-compatible API format for easy integration with existing code.
- Generous free tier for experimentation and community-driven model ecosystem.

**Best for:** Teams wanting cutting-edge open-source models, developers needing flexibility between hosted and self-hosted options, budget-conscious teams, and experimentation with new architectures.

[⬆️ Up](#table-of-contents)

---

## **5. Appendices**

### **5.1. Additional Coding Agents**

Inconclusive list of additional coding agents (most of them are not CLI coding agents but IDE or web-based tools).

---

#### **1. Windsurf Editor**
- **Organisation:** [Cognition](https://cognition.ai) (formerly [Windsurf](https://windsurf.com/))
- **Website:** https://windsurf.com/editor
- **GitHub:** ❌ Not open-source (proprietary)
- **Project Type:** Standalone IDE Application
- **Project Context:** Standalone project (planned integration into Cognition's platform as [Devin](https://devin.ai/))
- **Description:** AI-powered IDE with agentic capabilities and multi-file editing. Standalone application, not a CLI tool.
- **Pricing:** Free tier available. [Pricing details](https://windsurf.com/pricing)
- **Note:** Not a CLI tool

[⬆️ Up](#table-of-contents)

---

#### **2. Roo Code**
- **Organisation:** [Roo Code](https://roocode.com/)
- **Website:** https://roocode.com/
- **GitHub:** https://github.com/RooCodeInc/Roo-Code (⭐ ~3.5k)
- **Project Type:** VS Code Extension
- **Project Context:** Standalone project
- **Description:** AI coding assistant VS Code extension focused on agentic workflows and codebase understanding. No standalone CLI interface.
- **Pricing:** Free tier + subscription plans. [Pricing details](https://roocode.com/pricing)
- **Note:** Not a CLI tool

[⬆️ Up](#table-of-contents)

---

#### **3. Replit Agent**
- **Organisation:** [Replit](https://replit.com)
- **Website:** https://replit.com
- **GitHub:** ❌ Not open-source (proprietary)
- **Project Type:** Cloud IDE Integration
- **Project Context:** Component of Replit cloud IDE platform
- **Description:** Browser-based AI coding agent integrated into Replit's cloud IDE. Code lives in Replit's cloud infrastructure. No standalone CLI interface.
- **Pricing:** Included with Replit subscription tiers. [Pricing details](https://replit.com/pricing)
- **Note:** Not a CLI tool

[⬆️ Up](#table-of-contents)

---

#### **4. cto.new**
- **Organisation:** [Engine Labs](https://github.com/Engine-Labs) (United Kingdom)
- **Website:** https://cto.new
- **GitHub:** ❌ Not open-source (proprietary)
- **Project Type:** Web-based Platform
- **Project Context:** Standalone project
- **Description:** Browser-based AI coding platform that executes code changes in cloud VMs and opens PRs. Intended to be free and unlimited for GPT-5, Claude Sonnet 4.5, and Gemini 2.5 Pro in exchange for using user data for model training. Not yet generally available.
- **Pricing:** Free (planned, ad-supported, waitlist available)
- **Note:** Not a CLI tool

[⬆️ Up](#table-of-contents)

---

#### **5. Qwen Code**
- **Organisation:** [Alibaba Cloud](https://www.alibabacloud.com) (QwenLM)
- **Website:** https://qwenlm.github.io/qwen-code-docs/en/
- **GitHub:** https://github.com/QwenLM/qwen-code (⭐ ~2.9k)
- **Project Type:** CLI Coding Agent
- **Project Context:** Component of Qwen suite (includes [Qwen Chat](https://chat.qwen.ai/))
- **Description:** Open-source coding assistant powered by Qwen language models with CLI interface and IDE integrations.
- **Pricing:** Free (open-source)
- **Note:** Chinese project

[⬆️ Up](#table-of-contents)

---

#### **6. CodeBuddy CLI**
- **Organisation:** [Tencent](https://www.tencent.com)
- **Website:** https://www.codebuddy.ai/cli
- **GitHub:** ❌ Not open-source (proprietary)
- **Project Type:** CLI Coding Agent
- **Project Context:** Component of CodeBuddy AI platform
- **Description:** Tencent's AI coding assistant with command-line interface for terminal-based development workflows.
- **Pricing:** Free tier + Pro ($19.99/month) + Teams ($29.99/user/month). [Pricing details](https://www.codebuddy.ai/pricing)
- **Note:** Chinese project

[⬆️ Up](#table-of-contents)

---