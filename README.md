# Anti-AI Slop: Production Web Interface Design Rules & Skill

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Skills Compatibility](https://img.shields.io/badge/Skills-Antigravity%20%7C%20Claude%20Code%20%7C%20Cursor%20%7C%20Windsurf-success.svg)](#installation)

> **Eliminate the telltale signs of AI-generated web templates. Enforce restrained, intentional, production-grade craft.**
>
> **دليل ومهارة تصميم برمجية لمنع مخرجات الذكاء الاصطناعي النمطية (AI Slop) وإنتاج واجهات ويب حقيقية واحترافية.**

---

## The Problem (المشكلة)

When modern AI models generate web interfaces, they suffer from deep statistical biases that make the output immediately recognizable within seconds:
- **Blue-to-purple and indigo-to-violet gradients** on every button, background, and text header.
- **Sparkles and shimmers (`✨`, `✦`, `🪄`)** sprinkled across every feature and badge.
- **Inflated hype copy:** *"Unleash"*, *"Supercharge"*, *"Seamlessly unlock your full potential"*.
- **Heavy decorative drop-shadows** and rainbow-coloured card grids.
- **Icons imprisoned in tinted pastel rounded squares**.
- **Rigid boilerplate structures:** *Hero → Logo strip → 3 cards → Quote → 3 pricing tiers → FAQ*.

The result is "AI Slop" — interfaces that look like cheap templates and erode user trust.

---

## The Solution (الحل)

This repository provides **strict, non-negotiable craft constraints** that replace decorative defaults with deliberate, production-ready human decisions (similar to software built by Stripe, Linear, and Vercel).

Available in two formats:
1. **`SKILL.md`**: An autonomous **Agent Skill** compatible with Google Antigravity, Claude Code, and agentic workflows. It triggers automatically whenever you design, style, or review frontend code.
2. **`DESIGN_RULES.md`**: A standalone reference document to drop into project roots, `CLAUDE.md`, `GEMINI.md`, or `.cursorrules`.

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

## Installation & Usage (طريقة التثبيت والاستخدام)

### Option 1: Antigravity / Gemini CLI (`agy`)

To install globally for all your projects:

#### Windows (PowerShell):
```powershell
New-Item -ItemType Directory -Force -Path "$HOME\.gemini\config\skills\anti-ai-slop"
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/MosaabGalmod/anti-ai-slop/main/SKILL.md" -OutFile "$HOME\.gemini\config\skills\anti-ai-slop\SKILL.md"
```

#### macOS / Linux:
```bash
mkdir -p ~/.gemini/config/skills/anti-ai-slop
curl -sSL https://raw.githubusercontent.com/MosaabGalmod/anti-ai-slop/main/SKILL.md -o ~/.gemini/config/skills/anti-ai-slop/SKILL.md
```

Once installed, Antigravity will automatically load and enforce the skill whenever you build or edit UI components.

---

### Option 2: Claude Code

Add as a personal skill:

```bash
mkdir -p ~/.claude/skills/anti-ai-slop
curl -sSL https://raw.githubusercontent.com/MosaabGalmod/anti-ai-slop/main/SKILL.md -o ~/.claude/skills/anti-ai-slop/SKILL.md
```

Or append the rules directly to your global `~/.claude/CLAUDE.md`:
```bash
curl -sSL https://raw.githubusercontent.com/MosaabGalmod/anti-ai-slop/main/DESIGN_RULES.md >> ~/.claude/CLAUDE.md
```

---

### Option 3: Cursor, Windsurf, or VS Code

Place `DESIGN_RULES.md` in your project root, or copy its content into `.cursorrules` / `.windsurfrules`:

```bash
curl -sSL https://raw.githubusercontent.com/MosaabGalmod/anti-ai-slop/main/DESIGN_RULES.md -o .cursorrules
```

---

### Option 4: Direct Prompting (v0, ChatGPT, Claude.ai, Gemini)

Copy the raw text of [`DESIGN_RULES.md`](DESIGN_RULES.md) and paste it at the beginning of your prompt:

```text
You are building a production web interface. The following rules are hard constraints, not suggestions...
[Paste DESIGN_RULES.md here]
```

---

## Pre-Completion Audit Checklist (قائمة التحقق قبل التسليم)

Before shipping any UI code, review against these 14 audit questions:

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

**Rule:** If a reviewer could tell the page was generated by AI in under 5 seconds, find the specific tell and fix it.

---

## License

This project is licensed under the [MIT License](LICENSE) — free to use in personal, open-source, and commercial projects.
