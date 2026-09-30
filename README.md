# Anti-AI Slop: Universal Agent Skill & Craft Design Rules

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Skills Compatibility](https://img.shields.io/badge/Universal%20Agents-Antigravity%20%7C%20Claude%20Code%20%7C%20Codex%20%7C%20Cursor%20%7C%20Windsurf%20%7C%20Cline%20%7C%20Copilot-success.svg)](#installation--agent-setup)

> **Eliminate the telltale signs of AI-generated web templates. Enforce restrained, intentional, production-grade craft across ALL AI coding agents.**
>
> **دليل ومهارة تصميم برمجية عامة وشاملة لكافة الوكلاء الأذكياء (Claude Code, Antigravity, OpenAI Codex, Cursor, Windsurf, Cline, Copilot) لمنع مخرجات الذكاء الاصطناعي النمطية (AI Slop) وإنتاج واجهات ويب حقيقية واحترافية.**

---

## The Problem (المشكلة)

When modern AI agents generate web interfaces, they suffer from deep statistical biases that make their output immediately recognizable within seconds:
- **Blue-to-purple and indigo-to-violet gradients** on every button, background, and text header.
- **Sparkles and shimmers (`✨`, `✦`, `🪄`)** sprinkled across every feature and badge.
- **Inflated hype copy:** *"Unleash"*, *"Supercharge"*, *"Seamlessly unlock your full potential"*.
- **Heavy decorative drop-shadows** and rainbow-coloured card grids.
- **Icons imprisoned in tinted pastel rounded squares**.
- **Rigid boilerplate structures:** *Hero → Logo strip → 3 cards → Quote → 3 pricing tiers → FAQ*.

The result is "AI Slop" — interfaces that look like cheap templates and erode user trust.

---

## Universal Multi-Agent Architecture (البنية الشاملة للوكلاء)

This repository is designed from the ground up to be **universal**, adhering to both the **Agent Skills specification** and the **`AGENTS.md` open standard**:

```text
anti-ai-slop/
├── SKILL.md                  # Autonomous skill for Antigravity & Claude Code
├── AGENTS.md                 # Universal open standard for modern coding agents (Codex, etc.)
├── DESIGN_RULES.md           # Standalone raw rules for system prompts and constitution
├── install.ps1               # 1-Click universal installer for Windows
├── install.sh                # 1-Click universal installer for macOS / Linux
├── adapters/
│   ├── .cursorrules          # Turnkey rule adapter for Cursor IDE
│   ├── .windsurfrules        # Turnkey rule adapter for Windsurf / Cascade
│   ├── .clinerules           # Turnkey rule adapter for Cline / Roo Code
│   └── copilot-instructions  # Turnkey rule adapter for GitHub Copilot
└── docs/
    └── CONVERSATION.md       # Genesis record, analysis, and execution history
```

---

## Core Rules at a Glance (أبرز القواعد)

| Domain | Rule | Banned Tropes |
|---|---|---|
| **Colour** | 1 accent colour (<10% surface). Single neutral family. | Purple/indigo gradients, gradient text, rainbow feature grids. |
| **Depth** | 1px borders, subtle background steps, whitespace. | Drop-shadows on cards/inputs/buttons (shadows only on real modals/popovers). |
| **Icons & Emoji** | Monochrome icons at text size inheriting `currentColor`. | Sparkles (`✨`), emoji in UI (🚀, ⚡), icons in tinted pastel rounded boxes. |
| **Typography** | Concrete nouns, real numbers, 1-2 type families, 12-48px scale. | Buzzwords (*supercharge, unleash, seamless*), em dashes (`—`) in UI copy. |
| **Motion** | Restrained 120-160ms ease-out transitions on border/color. | Sliding button arrows, hover glow/halo/scale, bouncy chevrons, idle loops. |
| **Scale** | Hero headline 40-56px desktop. 4px spatial rhythm. | 72px+ giant headlines, 160px+ padding, full-viewport `100vh` hero traps. |
| **Layout** | Content-driven grid shapes and natural section flow. | Generic eyebrow pill badges (*"Introducing v2.0"*), cookie-cutter template orders. |
| **Placeholders** | Specific company names, precise metrics, real empty/error states. | Generic *"Company A"*, round *"10,000+"* placeholders, missing edge states. |
| **Code Craft** | Semantic HTML, accessible `:focus-visible`, logical CSS (RTL/LTR). | Clickable `<div>`, unlabelled images, arbitrary inline values, low contrast. |

---

## ⚡ 1-Click Installation (التثبيت السريع بأمر واحد)

### Windows (PowerShell):
```powershell
irm https://raw.githubusercontent.com/MosaabGalmod/anti-ai-slop/main/install.ps1 | iex
```

### macOS / Linux (Bash):
```bash
curl -fsSL https://raw.githubusercontent.com/MosaabGalmod/anti-ai-slop/main/install.sh | bash
```

The script automatically detects your tools and installs the skill/rules to **Antigravity**, **Claude Code**, **Cursor**, **Windsurf**, and **Cline**.

---

## Manual Agent Setup (الإعداد اليدوي حسب الأداة)

### 1. Google Antigravity & Gemini CLI (`agy`)
Install globally:
```powershell
New-Item -ItemType Directory -Force -Path "$HOME\.gemini\config\skills\anti-ai-slop"
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/MosaabGalmod/anti-ai-slop/main/SKILL.md" -OutFile "$HOME\.gemini\config\skills\anti-ai-slop\SKILL.md"
```

### 2. Claude Code
Install as a personal skill:
```bash
mkdir -p ~/.claude/skills/anti-ai-slop
curl -sSL https://raw.githubusercontent.com/MosaabGalmod/anti-ai-slop/main/SKILL.md -o ~/.claude/skills/anti-ai-slop/SKILL.md
```
Or append to your global `~/.claude/CLAUDE.md`:
```bash
curl -sSL https://raw.githubusercontent.com/MosaabGalmod/anti-ai-slop/main/DESIGN_RULES.md >> ~/.claude/CLAUDE.md
```

### 3. OpenAI Codex & Universal Agents (`AGENTS.md`)
Drop `AGENTS.md` into the root of any repository. Modern agents automatically parse and obey it:
```bash
curl -sSL https://raw.githubusercontent.com/MosaabGalmod/anti-ai-slop/main/AGENTS.md -o AGENTS.md
```

### 4. Cursor IDE
Download `.cursorrules` to your project root:
```bash
curl -sSL https://raw.githubusercontent.com/MosaabGalmod/anti-ai-slop/main/adapters/.cursorrules -o .cursorrules
```

### 5. Windsurf / Cascade
Download `.windsurfrules` to your project root:
```bash
curl -sSL https://raw.githubusercontent.com/MosaabGalmod/anti-ai-slop/main/adapters/.windsurfrules -o .windsurfrules
```

### 6. Cline & Roo Code
Download `.clinerules` to your project root:
```bash
curl -sSL https://raw.githubusercontent.com/MosaabGalmod/anti-ai-slop/main/adapters/.clinerules -o .clinerules
```

### 7. GitHub Copilot
Add to `.github/copilot-instructions.md`:
```bash
mkdir -p .github
curl -sSL https://raw.githubusercontent.com/MosaabGalmod/anti-ai-slop/main/adapters/copilot-instructions.md -o .github/copilot-instructions.md
```

### 8. Web Platforms (v0, ChatGPT, Claude.ai, Gemini)
Copy the raw text of [`DESIGN_RULES.md`](DESIGN_RULES.md) into your prompt or Custom Instructions.

---

## Pre-Completion Audit Checklist (قائمة التحقق قبل التسليم)

Before declaring any UI complete, verify against these 14 audit questions:

- [ ] 1. Any blue-to-purple or indigo-to-violet gradient left, anywhere?
- [ ] 2. Any gradient text (`background-clip: text`)?
- [ ] 3. Does anything that is not a floating overlay (modal, popover, toast) have a shadow?
- [ ] 4. Any sparkle glyph (`✨`, `✦`, `🪄`)?
- [ ] 5. Any emoji used as interface?
- [ ] 6. Does any icon sit inside a tinted square, circle, or box?
- [ ] 7. Any em dash (`—`) in UI copy?
- [ ] 8. Any hits from the banned word list (*unleash, supercharge, seamless...*)?
- [ ] 9. Does each feature or category have its own decorative colour?
- [ ] 10. Does any button contain a moving arrow on hover?
- [ ] 11. Does anything glow, lift, or scale on hover?
- [ ] 12. Is there an eyebrow badge above the hero that says nothing?
- [ ] 13. Is the hero headline above 56px, or any section over 96px of vertical padding?
- [ ] 14. Does any element look oversized next to the text beside it?

**Core Standard:** If a reviewer could tell the page was generated by AI in under 5 seconds, identify the specific giveaway and replace it with intentional craftsmanship.

---

## License

This project is licensed under the [MIT License](LICENSE) — free to use in personal, open-source, and commercial projects.
