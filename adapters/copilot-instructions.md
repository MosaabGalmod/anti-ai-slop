# GitHub Copilot Instructions: Anti-AI Slop Craft Standards

## UI / Frontend Code Generation Guidelines
When writing HTML, JSX, Vue, Svelte, CSS, or Tailwind markup:

1. **Colour Tokens**:
   - Limit accent colour to ONE primary accent, keeping surface usage under 10%.
   - Strictly prohibit blue→purple and indigo→violet gradients anywhere.
   - Prohibit gradient text (`background-clip: text`).
   - Keep feature cards monochromatic and consistent; do not assign distinct colours to each card.

2. **Depth & Shadows**:
   - Zero drop-shadows on stationary cards, inputs, badges, or buttons.
   - Use subtle shadows (`0 1px 2px rgba(0,0,0,0.06)`) only on floating overlays (modals, popovers, dropdowns).
   - Prefer 1px borders or subtle background tint steps for block separation.

3. **Icons & Glyphs**:
   - Never use sparkle glyphs (`✨`, `✦`, `🪄`) for AI features; describe them in clear words.
   - Never use emoji as UI elements (no 🚀, ⚡, 🎯, 🔥 in buttons, badges, or headings).
   - Never wrap icons in tinted rounded square chip containers; place icons naked at text size.

4. **Typography & Copy**:
   - Ban buzzwords: *unleash, supercharge, elevate, transform, revolutionise, empower, seamless, effortless, cutting-edge, game-changing, next-level, unlock, harness, robust, leverage, powerful*.
   - Never use the em dash (`—`) in UI microcopy.
   - Keep hero text between 40-56px on desktop (never 72px+).

5. **Craft & Accessibility**:
   - Use semantic HTML tags. Never use a clickable `<div>` instead of a `<button>`.
   - Implement visible `:focus-visible` styles on all interactive elements.
   - Use CSS Logical Properties (`margin-inline-start`, `text-align: start`) for bidirectional (RTL/LTR) support.
