---
name: anti-ai-slop
description: Enforces authentic, production-grade UI design rules and eliminates generic AI aesthetic tropes (no purple gradients, no sparkles, no decorative shadows, restrained typography, semantic HTML, and RTL compatibility). Trigger automatically whenever designing, building, modifying, styling, or reviewing any web interface, page, or UI component.
---

# Anti-AI Slop Design System & Craft Guidelines

You are building a production web interface. The rules below are hard constraints, not suggestions. When a rule conflicts with what you were about to generate or what a default template provides, **the rule wins**.

The goal is not simply to "avoid a list of things." It is to make a deliberate, craft-focused choice in each place where the default would otherwise be mindless decoration. If you remove a banned element and put nothing considered in its place, the result is worse, not better.

---

## 1. Colour Tokens & Accent Discipline

- **One Accent Colour:** Choose exactly ONE accent colour for the entire interface. Everything else is neutral, drawn from a single family of greys with a consistent temperature (all warm or all cool, never mixed).
- **Semantic Secondary Colours Only:** A second colour is allowed only when it carries objective functional meaning: destructive/error (red), success (green), warning (amber). Never introduce a colour for variety or novelty.
- **Banned Gradients:** Blue-to-purple (`#2563eb` → `#9333ea`) and indigo-to-violet gradients are strictly forbidden anywhere. This includes backgrounds, buttons, headings, logos, icons, borders, blurred "blobs", and mesh backgrounds.
- **Banned Gradient Text:** Gradient text (`background-clip: text` with transparent fill) is banned. All headings and text must be solid, high-contrast colours.
- **Unified Feature Palette:** Banned: giving each feature, category, or card its own distinct hue (e.g. rainbow card decks). A feature grid must use the exact same neutral surface and colour scheme across all cards. Colour encodes meaning, not decorative variety.
- **No Untouched Framework Palettes:** Do not ship Tailwind's default palette untouched (`indigo-600`, `violet-500`, `slate-900` is the single most recognizable AI signature). Define deliberate, project-specific design tokens.
- **Accent Surface Budget:** Keep accent colour usage strictly under 10% of the visible surface area. If a page looks colourful at a glance, the accent colour has been overused.

---

## 2. Depth, Surfaces & Shadows

- **No Fake Shadows:** A drop shadow is banned on anything that is not genuinely floating in the viewport z-axis. Cards, sections, containers, images, input fields, badges, and static buttons get zero shadow (`box-shadow: none`).
- **Permitted Shadows (Overlays Only):** Shadows are permitted exclusively on elements that physically overlay page content: dropdown menus, popovers, dialogs/modals, and toast notifications.
- **Tight, Subtle Elevation:** When a shadow is permitted, keep it tight and low-opacity (e.g. `0 1px 2px rgba(0, 0, 0, 0.06)` or `0 4px 12px rgba(0, 0, 0, 0.08)`). A 40px coloured bloom is strictly banned. Never stack multiple shadows to simulate fake depth.
- **Real Separation Hierarchy:** Separate blocks and cards using the following order of preference:
  1. Whitespace (the best separator, zero visual noise).
  2. A subtle 1px border (`border: 1px solid var(--border)`).
  3. A single background step (`bg-neutral-50` vs `bg-white` or `neutral-900` vs `neutral-950`).
- **Consistent Radius and Border:** Pick exactly one border-radius value (e.g. `6px` or `8px`) and one border colour, and apply them consistently across all inputs, cards, and buttons.

---

## 3. Icons, Glyphs & Emoji

- **Banned AI Shimmer & Sparkles:** The sparkle icon (`✨`, `✦`, `✧`, `🪄`) and any "AI shimmer" glyph are banned across buttons, badges, logos, navigation, headings, and beside product names. The sparkle-as-AI icon is the clearest indicator of an AI-generated site. If a feature uses machine learning or automation, describe what it does in plain words.
- **Banned Emoji as Interface:** Emoji are banned in headings, buttons, feature lists, badges, tabs, navigation, or empty states (no `🚀`, `⚡`, `🎯`, `🔥`, `💡`). Emoji belong in user content, never in a production interface.
- **No Icon Container Chips:** Any container around an icon is banned. No tinted rounded squares, no pastel circles, no bordered boxes, no coloured background chips behind icons. The icon sits directly on the background at text size. The icon-in-a-soft-tinted-square is an overused template signature.
- **Unified Icon System:** Use a single production icon set (Lucide, Heroicons, or Phosphor) with a consistent stroke weight (typically 1.5px or 1.75px). Render icons in monochrome inheriting `currentColor`, sized proportionally to the adjacent text.
- **Label Clarity First:** If a feature or button is self-evident from its label, omit the icon entirely.

---

## 4. Typography, Measure & Copywriting

- **Banned AI Buzzwords:** The following words are banned in both UI copy and marketing headings:
  > *unleash, supercharge, elevate, transform, revolutionise, empower, seamless, effortless, effortlessly, cutting-edge, game-changing, next-level, unlock, harness, robust, leverage, powerful, delve, paradigm, synergy.*
  > 
  > *Rule of thumb:* If a sentence survives deleting the adjective, delete the adjective.
- **Banned Em Dash in UI:** The em dash (`—`) is banned in UI copy, microcopy, headings, tooltips, and empty states. Write two distinct sentences, or use a comma or parentheses.
- **Concrete Nouns & Real Numbers:** State what the product actually does. Example: *"Export transactions to CSV in one click"* beats *"Seamlessly unlock your financial data's full potential."*
- **Typographic Scale:** Limit the project to one type family (at most two: one UI sans-serif, one monospace for data/code). Adhere to a strict, stepped scale: `12 / 14 / 16 / 20 / 24 / 32 / 48px`. Avoid arbitrary intermediate sizes.
- **Alignment & Reading Measure:** Body text must be aligned to the reading start (left-aligned for LTR, right-aligned for RTL). Center only short headings (1-2 lines). Never center a paragraph longer than three lines. Cap body text measure at ~65-75 characters per line (`max-w-prose` / `max-width: 65ch`).
- **Sentence Case:** Use sentence case for headings, labels, and buttons. Avoid Title Case Everywhere, and never use ALL-CAPS except for tracked micro-labels (`tracking-wider text-xs uppercase`).

---

## 5. Motion, States & Transitions

- **Banned Button Animations:** An arrow inside a button that slides on hover is banned. Bouncing chevrons, arrows that animate on their own, and looping idle motions are banned.
- **Banned Hover Effects:** Hover glow, box-shadow blooms, coloured halos, `scale()` transforms above 1.02, and card-lifting hover transitions are banned.
- **Clean Interactive States:** Hover states should change background or border colour only, using a subtle duration of 120-160ms with `ease-out`.
- **Restrained Animation Properties:** Animate `opacity` and `transform` exclusively. Durations: 120-200ms for UI feedback, up to 300ms for entering dialogs or drawers. Avoid easing curves lasting 500ms or longer.
- **No Scroll Gimmicks:** No scroll-triggered fade-ins on every section. No parallax backgrounds. No typewriter effects, no ticking-up numbers, no infinite marquee strips of company logos.
- **Respect Motion Preferences:** Always wrap animations in `@media (prefers-reduced-motion: reduce)` to disable or flatten non-essential motion.

---

## 6. Scale, Proportions & 4px Rhythm

Nothing should be oversized. Everything must be sized to fit its content neatly. Inflated typography, padding, and buttons announce an automated template before a single word is read.

- **Hero Headline:** 40-56px on desktop, 28-34px on mobile. Never 72px+. A headline does not need to fill the entire viewport height to be impactful.
- **Body & Secondary Text:** Body text is 15-16px. Secondary/caption text is 13-14px. Nothing readable below 12px.
- **Button Sizing:** 36-44px tall, with horizontal padding sized to the text label. Never full-width on desktop. A primary button and a secondary outline/ghost button are sufficient.
- **Section Vertical Padding:** 64-96px on desktop, 40-56px on mobile. Avoid massive 160px+ empty vertical gaps.
- **Container Max-Width:** 1100-1280px maximum. Never allow a line of text or card grid to stretch across the full width of an ultrawide or 1920px screen.
- **Icon Sizing:** Inline icons 16-20px; standalone feature icons 24px. No 48px+ decorative floating icons.
- **No Full-Viewport Hero Trap:** Avoid forcing the hero section to `100vh` just for dramatic effect. The hero must visually hint that real content continues below the fold.
- **Card Heights:** Cards must be sized by their internal content. Do not force artificial equal heights unless the content items are genuinely identical.
- **4px Spatial Grid:** Every margin, padding, gap, and dimension must be a multiple of 4px (`4, 8, 12, 16, 24, 32, 48, 64px`). Align related elements to consistent start and baseline edges.

---

## 7. Layout Structure & Template Cliché Elimination

- **Banned Eyebrow Pill Badge:** Banned: the generic pill badge floating above the hero headline reading *"Introducing v2.0"*, *"AI-Powered"*, *"New"*, or *"Trusted by 10,000+ developers"*. If a piece of information is critical, place it directly in the headline; if not, remove it.
- **Break the Cliché Template Sequence:** Do not blindly generate the standard sequence:
  > *Hero → Monochromatic logo strip → 3 feature cards → 1 customer quote → 3 pricing tiers → Accordion FAQ → Repeated CTA banner.*
  
  Build only the specific sections this product actually requires, in the logical sequence a prospective user or operator needs to evaluate it.
- **Organic Content-Driven Grids:** Feature layouts do not have to be rigid 3-column cards of identical length. Let real data, metrics, code snippets, or workflows determine card geometry.
- **Restraint Over Uniformity:** Not every container needs to be a bordered card, not every layout needs to be centered, and not every corner needs full rounding.

---

## 8. Specific Placeholder & Edge States

- **Specific Over Generic Placeholders:** If demo content is needed, avoid generic placeholders like *"Acme Corp"*, *"Company A"*, or generic stock names. Use plausible, industry-specific names, realistic testimonial text referencing concrete workflows, and natural, non-round numbers (e.g. `99.94%` or `1,420` instead of `10,000+`).
- **Placeholder Copy Discipline:** Placeholder copy must obey all typography rules: no hype adjectives, no em dashes, and no emoji.
- **First-Class Edge States:** Every UI surface must include well-designed, functional edge states:
  - Empty states (with a clear, single-click action to create or import).
  - Error states (actionable explanation with recovery paths).
  - Loading skeletons (restrained, matching the exact shape of incoming content).

---

## 9. Code Craft, Accessibility & RTL Support

- **Semantic HTML Only:** Use semantic tags (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<button>`, `<a>`). A clickable `<div>` or `<span>` without button semantics and keyboard handlers is a critical bug.
- **Visible Focus States:** Provide clear, high-contrast `:focus-visible` styling on all interactive elements. Ensure keyboard navigation order mirrors the visual layout.
- **Image Accessibility:** Every informative image must feature descriptive `alt` text. Purely decorative elements must have `alt=""` and `aria-hidden="true"`.
- **WCAG Contrast Ratios:** Ensure contrast ratios reach at least 4.5:1 for standard body text and 3:1 for large text and interactive boundaries.
- **Component Hygiene:** Extract repeated markup into reusable components if it appears three or more times. Rely on design tokens or CSS custom properties, never arbitrary one-off inline values.
- **Banned Native Blocking Alerts & Default Popups:** `window.alert()`, `window.confirm()`, `window.prompt()`, and unstyled browser default validation balloons (from unhandled `required` attributes) are strictly banned. They halt the JavaScript execution thread, violate theme tokens, break dark/light modes, and corrupt bidirectional RTL continuity. Use non-blocking, accessible custom toast notifications and inline field validation tied with `aria-describedby` and `novalidate` forms.
- **Full BiDi & RTL Support:**
  - Use CSS Logical Properties (`margin-inline-start`, `padding-inline-end`, `inset-inline-start`, `text-align: start`) instead of physical `left` and `right`.
  - When rendering Arabic text, ensure `dir="rtl"` is set, text is right-aligned (`text-align: right/start`), and Western digits or Latin symbols are isolated (`<bdi>` or `dir="ltr"`).

---

## 10. Pre-Completion Audit Checklist

Before declaring any UI task or component complete, review every line against these 15 audit questions:

| # | Inspection Question | Status |
|---|---------------------|:------:|
| 1 | Is there any blue-to-purple or indigo-to-violet gradient anywhere? | Must be NO |
| 2 | Is there any gradient text (`background-clip: text`)? | Must be NO |
| 3 | Does anything that is not a floating overlay (modal, popover, toast) have a shadow? | Must be NO |
| 4 | Is there any sparkle, star, or AI shimmer glyph (`✨`, `✦`, `🪄`)? | Must be NO |
| 5 | Is any emoji used as an interface element, icon, or badge? | Must be NO |
| 6 | Does any icon sit inside a tinted square, circle, or coloured background chip? | Must be NO |
| 7 | Is there any em dash (`—`) in UI copy or microcopy? | Must be NO |
| 8 | Does the copy contain any banned buzzwords (*unleash, supercharge, seamless, etc.*)? | Must be NO |
| 9 | Does each card or category have its own decorative colour hue? | Must be NO |
| 10 | Does any button contain a sliding arrow or bouncy animation on hover? | Must be NO |
| 11 | Does any card or button glow, lift, or scale on hover? | Must be NO |
| 12 | Is there an empty eyebrow pill badge above the hero? | Must be NO |
| 13 | Is the hero headline over 56px, or does any section have vertical padding over 96px? | Must be NO |
| 14 | Does any element look disproportionately oversized relative to its adjacent content? | Must be NO |
| 15 | Is `window.alert()`, `window.confirm()`, or browser default `required` popup used anywhere? | Must be NO |

If a reviewer could identify that the page was generated by AI in under five seconds, pinpoint the exact telltale pattern and replace it with intentional, production-grade craft.
