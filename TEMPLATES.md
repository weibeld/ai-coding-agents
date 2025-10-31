# Documentation Templates and Tokens

This file contains standardized text tokens and templates used throughout the documentation. Always use these exact formats for consistency.

## Markdown Formatting Rules

**Headers:**
- Always add an empty line below markdown headers (#, ##, ###, ####)

**Term explanations:**
- Use colons instead of dashes for term explanations
- Example: "**foo:** bar" NOT "**foo** - bar"

## Agent Categories

Use these exact tokens when categorizing agents:

```
⚡️ CLI Agent
🧩 IDE Extension
🖥️ Dedicated IDE
🌍 Web IDE
⚙️ Other
```

**Examples:**
- `**Type:** ⚡️ CLI Agent`
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
