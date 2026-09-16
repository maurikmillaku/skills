# web-craft

A self-contained agent skill that elevates any existing website to world-class software standards.

Most websites look fine on a laptop, but as soon as you open them on a phone, they feel cheap. Buttons lag, hovers get stuck, inputs zoom in and break your layout, and the contrast is washed out.

I built this skill because I wanted every website I work on to feel like high-end software: fast, tactile, responsive, and completely free of the little bugs that give web apps a bad name.

You do not need to install five different skills or rebuild your entire site from scratch. You install this one skill, and your AI agent gets the complete playbook: every diagnostic check, CSS rule, tactile detail, and contrast token needed to level up your existing site.

---

## What It Covers

1. **Touch & Platform Defect Eradication**:
   - Removes the blue and gray tap highlight box on phones.
   - Kills sticky hover states on touchscreens.
   - Stops iOS Safari from auto-zooming on inputs with a 16px font rule.
   - Fixes mobile viewport overflow with `100dvh` and `100svh`.
   - Handles device display notches and safe areas properly.
   - Solves browser status bar color mismatches.

2. **Tactile Micro-Interactions & Spring Physics**:
   - Instant response on finger touchdown instead of waiting for mouse-up.
   - Physical active scale compression (`scale(0.96)` to `scale(0.97)`).
   - Fast cubic-bezier transition curves that settle smoothly without bounce fatigue.
   - Strict GPU compositing rules (`transform` and `opacity` only).

3. **Midnight Monochrome Contrast System**:
   - Pitch-black obsidian dark mode paired with crisp hairline borders.
   - High-contrast, clean light mode.
   - Zero-flash theme persistence script to stop light and dark flashes on page load.
   - Keyboard-friendly tactile theme toggle helper.

4. **Command Palette & Global Search**:
   - Quick search and action palette triggered with `Cmd+K` or `Ctrl+K`.
   - Focuses cleanly without causing page scroll jumps (`preventScroll: true`).
   - Renders through a document portal so ancestor styles never clip or blur it.
   - Keeps mobile headers uncluttered by hiding keyboard shortcut badges on phone screens.

5. **Sub-Second Speed & Perceived Latency**:
   - Quarantines expensive blur filters to the floating top bar so mobile scrolling stays at 60 to 120 FPS.
   - Prevents layout shifts during font loading.
   - Instant optimistic feedback on user actions.

6. **Typography, Punctuation, & Copy Hygiene**:
   - Zero em-dashes: replaced with commas, parentheses, or clean sentence breaks.
   - Zero directional UI arrows: interactive elements rely on clean typography, contrast, and spacing.
   - Anti-AI copy standards: direct, grounded, human writing focused on real outcomes instead of corporate buzzwords.

---

## Installation

Install using the skills CLI:

```bash
npx skills add maurikmillaku/skills --skill web-craft
```

Or copy `SKILL.md` directly into your project at `.agents/skills/web-craft/SKILL.md`.

---

## Author

**Maurik Millaku**
- Website: [maurikmillaku.com](https://maurikmillaku.com)
- GitHub: [@maurikmillaku](https://github.com/maurikmillaku)
- X: [@maurikmillaku](https://x.com/maurikmillaku)
- Email: millakumaurik@gmail.com
