# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **living documentation repository** that provides comprehensive comparisons and analysis of AI coding agents. The documentation is designed to be maintained and updated by AI agents to keep it current with the rapidly evolving ecosystem.

**Definition of Coding Agent:**

A coding agent is any agent that is mainly intended for writing code and targeted at developers. This EXCLUDES:
- Pure vibe coding agents
- Pure chat agents
- Integrated platforms aimed at creating full-stack apps including deployments

## Agent Categories

All coding agents are categorized into:
1. **⚡️ CLI agent:** Command-line interface tools
2. **🧩 IDE extension:** Plugins for existing IDEs (VS Code, JetBrains, etc.)
3. **🖥️ Local IDE:** Standalone IDE applications that run locally
4. **🌍 Web IDE:** Browser-based IDE environments
6. **⚙️  Other:** Tools that don't fit the above categories (e.g., GitHub UI integrations, management platforms)

## Pricing Models

All coding agents follow one of these pricing models:

**💸🆓 Pay for agent:**
- Users pay the agent provider
- Subscription or usage-based payment includes access to AI models
- Users typically do NOT need their own model API keys
- Agent provider manages model access and costs

**🆓💸 Pay for model:**
- The agent itself is free (or has optional paid tiers for extra features)
- Users pay model providers directly for model usage
- Users bring their own model API keys (BYOK)
- Agent provider does not charge for model access

## Required Information for Each Agent

When documenting or updating agents, always include:

**Basic Information:**
- Agent name
- Organization/Developer
- Website URL
- GitHub repository URL (if open-source)
- GitHub star count (format: ⭐ ~XXk)
- Open source status (Yes/No, with license if applicable)
- Agent category/type (with emoji)
- Introduction date (Month Year, e.g., "June 2025")

**Project Context:**
- Related tools from the same maker
- Whether it's a standalone project or part of a larger ecosystem
- Links to related offerings

**Model Access:**
- Which AI models are supported (OpenAI, Anthropic, Google, xAI, other providers)
- How models are accessed (native API, aggregator, BYOK, managed)
- Default model if applicable

**Pricing:**
- Pricing model: "Pay for agent" or "Pay for model"
- All pricing tiers with monthly/annual costs in USD
- Free tier details if available
- Links to official pricing pages

**Key Features:**
- Notable capabilities or differentiators
- Special modes or functionality
- Integration capabilities (MCP, Spec Kit, etc.)

**Release Information:**
- General availability date or beta status
- Major version milestones

## Update Instructions

For detailed instructions on how to update the documentation, see **UPDATE_INSTRUCTIONS.md**.

That file contains:
- Complete checklist of data points to verify and update
- Research methodology and information sources
- Update process and workflow
- Consistency requirements

## Documentation Standards

**Markdown Formatting:**
- Always add an empty line below markdown headers (#, ##, ###, ####)
- Use colons instead of dashes for term explanations: "**foo:** bar" not "**foo** - bar"

**Pricing Tables:**
- Right-align all numeric columns
- Use USD currency consistently
- Format model pricing as "per million tokens"

**Compatibility Indicators:**
- ✅ = Native support (direct API integration)
- 🔌 = Via aggregator (OpenRouter, etc.)
- ❌ = Not supported

**Links:**
- Maintain working hyperlinks to official sources
- Include pricing page links
- Include GitHub repository links where applicable

**Version Information:**
- Include "Last Updated: Month Day, Year" at top of comparison documents
- Track introduction dates and release dates for major features

## Future Plans

The documentation is currently published as GitHub Markdown files, but may later transition to a static website with additional functionality such as:
- Sortable and filterable tables
- Dynamic pricing comparisons
- Real-time updates
- Interactive compatibility matrices
