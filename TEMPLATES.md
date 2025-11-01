# Documentation Templates and Tokens

This file contains standardized text tokens and templates used throughout the documentation. Always use these exact formats for consistency.

## Agent Data Fields

This section defines all fields that should be collected for each coding agent.

### Core Information Fields

**Organisation:**
- Format: `**Organisation:** [Name](URL)`
- The company, organisation, or individual developer who creates and provides the agent

**Open-source:**
- Format: `**Open-source:** ✅ Yes` or `**Open-source:** ❌ No`
- Whether the agent is open-source

**GitHub repo:**
- Format: `**GitHub:** https://github.com/org/repo (⭐ ~XXk)` or `**GitHub:** ❌ None`
- GitHub repository URL if open-source, otherwise "❌ None"

**GitHub stars:**
- Format: `⭐ ~80.5k` or `⭐ ~4.1k` or `⭐ ~847` or `⭐ ~50`
- Include in GitHub repo field (see above)
- Use `~` for approximate, `k` for thousands
- Round to one decimal for 10k+, exact number for <1k
- This field should be sortable numerically

**Spec-driven development compatibility:**
- Format: Multiple sub-fields with ✅/❌ indicators
- Examples:
  - `**Spec Kit Compatible:** ✅`
  - `**OpenSpec Compatible:** ❌`
  - `**BetterSpec Compatible:** ✅`

**Website:**
- Format: `**Website:** https://example.com`
- Main website URL

**Project context:**
- Format: `**Project Context:** [description with links]`
- Whether it's a standalone project, part of a platform/suite, related tools
- Example: "Component of GitHub Copilot platform including [IDE extensions](URL), [Copilot Chat](URL)"

**Category:**
- Format: `**Type:** ⚡️ CLI Tool` (or other category emoji/name)
- See "Agent Categories" section for valid values

**IDE compatibility:**
- Format: `**IDE Compatibility:** VS Code, Cursor, Windsurf, JetBrains IDEs`
- Only applicable if Category is "🧩 IDE Extension"
- List of IDEs the extension supports

**Pricing model:**
- Format: `**Pricing Model:** 🕵️ Pay to Agent Provider` or `**Pricing Model:** 🏢 Pay to Model Provider`
- See "Pricing Models" section for valid values

**Free tier:**
- Format: `**Free Tier:** ✅ Yes` or `**Free Tier:** ❌ No`
- Only applicable if pricing model is "Pay to Agent Provider"

**Git integration:**
- Format: `**Git Integration:** ✅ GitHub, ✅ GitLab, ✅ Bitbucket, ✅ Self-hosted` or `**Git Integration:** ❌ No`
- Indicates if agent can commit to Git repositories
- If yes, list which Git hosting platforms are supported

**MCP support:**
- Format: `**MCP Support:** ✅ Yes` or `**MCP Support:** ❌ No`
- Whether the agent supports Model Context Protocol for extensibility

**Model selection:**
- Format: `**Model Selection:** User can select model` or `**Model Selection:** Model selected automatically`
- Whether users can choose models or if selection is automatic

**Model support:**
- Format: Table or structured list grouped by provider
- Groups: OpenAI, Google, Anthropic, xAI, Others
- For each model, indicate access method using compatibility indicators:
  - ✅ = Direct/native access through model provider
  - 🔌 = Via third-party aggregator (e.g., OpenRouter)
  - ❌ = Not supported
- May include comment in parentheses for how model is used
- Examples:
  - `✅ Claude Sonnet 4.5 (default)`
  - `✅ GPT-5 (Oracle subagent for reasoning)`
  - `🔌 Grok 3 (via OpenRouter)`

**Introduction date:**
- Format: `**Introduced:** June 2025` or `**Introduced:** 25 June 2025`
- See "Date Formats" section for formatting rules

### Pricing Table (only if "Pay to Agent Provider")

Use this table format for agents with "Pay to Agent Provider" pricing model:

```markdown
| Plan | Per Month (USD) | Per Year (USD) |
|------|----------------:|---------------:|
| [Free](URL) | $0  | $0   |
| [Pro](URL)  | $10 | $100 |
| [Pro+](URL) | $39 | $390 |
```

**Notes:**
- Link each plan name to the pricing details page
- Right-align numeric columns
- Use whole numbers (no decimals unless necessary)

## Markdown Formatting Rules

**Headers:**
- Always add an empty line below markdown headers (#, ##, ###, ####)

**Term explanations:**
- Use colons instead of dashes for term explanations
- Example: "**foo:** bar" NOT "**foo** - bar"

## Agent Categories

Use these exact tokens when categorizing agents:

```
⚡️ CLI Tool
🧩 IDE Extension
🖥️ Dedicated IDE
🌍 Web IDE
🔮 Vibe Coding
⚙️ Other
```

**Examples:**
- `**Type:** ⚡️ CLI Tool`
- `**Type:** 🧩 IDE Extension`

## Pricing Models

Use these exact tokens for pricing model classification:

```
🕵️ Pay to the agent provider
🏢 Pay to the model provider
```

**Examples:**
- `**Pricing Model:** 🕵️ Pay to the agent provider`
- `**Pricing Model:** 🏢 Pay to the model provider`

## Open Source Status

**For open-source projects:**
```
✅ Yes
```

**For proprietary projects:**
```
❌ No
```

## GitHub Information

**With repository:**
```
**GitHub:** https://github.com/org/repo (⭐ ~XXk)
```

**Without repository (proprietary):**
```
**GitHub:** ❌ None
```

**Star count formatting:**
- Use `~` for approximate
- Use `k` for thousands (e.g., ~40.4k, ~2.9k)
- Round to one decimal place for values over 10k
- For values under 1k, show exact number (e.g., ⭐ ~50, ⭐ ~847)

## Compatibility Indicators

Use these exact symbols:

```
✅ = Native support (direct API integration)
🔌 = Via aggregator (OpenRouter, etc.)
❌ = Not supported
```

**Examples:**
```
**Spec Kit Compatible:** ✅
**Spec Kit Compatible:** ❌
**Model Access:** ✅ Native API
**Model Access:** 🔌 Via OpenRouter
```

## Date Formats

**With day:**
```
**Introduced:** 25 June 2025
**Last Updated:** 27 October 2025
```

**Without day (month and year only):**
```
**Introduced:** June 2025
**Introduced:** October 2025
```

**Format:** dd MMMM yyyy OR MMMM yyyy (depending on whether day is known)

## Pricing Information

**Agent pricing table:**
```
| Plan | Per Month (USD) | Per Year (USD) |
|------|----------------:|---------------:|
| Free | $0              | $0             |
| Pro  | $10             | $100           |
| Pro+ | $39             | $390           |
```

**Notes:**
- Right-align numeric columns
- Use whole numbers for pricing (no decimals unless necessary)
- Include link to official pricing page below table

**Model pricing table:**
```
| Model | Input (USD/1M Tokens) | Output (USD/1M Tokens) | Context Size (Tokens) |
|-------|----------------------:|----------------------:|----------------------:|
```

**Notes:**
- Right-align all numeric columns
- Format: `$X.XX` for dollars
- Use "per 1M tokens" or "per million tokens"
- Separate input/output costs

## Model Provider Names

Use these exact names:

```
OpenAI
Anthropic
Google
xAI
Meta
Mistral
DeepSeek
```

## Common Model Names

**OpenAI:**
```
GPT-5
GPT-4.1
GPT-4o
GPT-4o Mini
o1
o3
o3-mini
o4-mini
```

**Anthropic:**
```
Claude Sonnet 4.5
Claude Sonnet 4
Claude 3.7 Sonnet
Claude Opus 4.1
Claude Opus 4
Claude Haiku 4.5
Claude Haiku 3.5
```

**Google:**
```
Gemini 2.5 Pro
Gemini 2.5 Flash
Gemini 2.0 Flash
Gemini Pro
```

**xAI:**
```
Grok 3
Grok 3 Mini
Grok Code Fast 1
Grok 4
Grok 4 Fast
```

## Pricing Table Headers

**For agent pricing:**
```
| Plan | Per Month (USD) | Per Year (USD) |
|------|------------------:|-----------------:|
```

**For model pricing:**
```
| Model | Input (USD/1M Tokens) | Output (USD/1M Tokens) | Context Size (Tokens) |
|-------|----------------------:|----------------------:|--------------------:|
```

## Links Format

**GitHub Issues/PRs:**
```
[github/spec-kit Issue #1021](https://github.com/github/spec-kit/issues/1021)
[github/spec-kit PR #677](https://github.com/github/spec-kit/pull/677)
```
