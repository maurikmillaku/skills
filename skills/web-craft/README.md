# web-craft

A self-contained agent skill that elevates any existing website to world-class software standards.

Most websites look fine on a laptop, but as soon as you open them on a phone, they feel cheap. Buttons lag, hovers get stuck, inputs zoom in and break your layout, and the contrast is washed out.

I built this skill because I wanted every website I work on to feel like high-end software: fast, tactile, responsive, and completely free of the little bugs that give web apps a bad name.

You do not need to install five different skills or rebuild your entire site from scratch. You install this one skill, and your AI agent gets the complete playbook: every diagnostic check, CSS rule, tactile detail, spring physics formula, optical typography standard, and contrast token needed to level up your existing site.

---

## What It Covers

1. **Touch & Platform Defect Eradication**:
   - Removes the blue and gray tap highlight box on phones.
   - Kills sticky hover states on touchscreens.
   - Stops iOS Safari from auto-zooming on inputs with a 16px font rule.
   - Fixes mobile viewport overflow with `100dvh` and `100svh`.
   - Handles device display notches and safe areas properly.
   - Solves browser status bar color mismatches.

2. **Fluid Physics, Springs, & Gestures**:
   - Instant response on finger touchdown instead of waiting for mouse-up.
   - Critically damped springs (damping 1.0, response 0.3s to 0.4s) for smooth, non-distracting motion.
   - Momentum flicks with velocity handoff so drag and release blend seamlessly.
   - Momentum projection formula that projects resting endpoints based on release speed.
   - Rubber-banding progressive resistance at boundaries rather than hard frozen stops.
   - Physical active scale compression (`scale(0.96)` to `scale(0.97)`).
   - Strict GPU compositing rules (`transform` and `opacity` only).

3. **Materials, Translucency, & Depth**:
   - Floating functional chrome with semi-transparent backgrounds and subtle blur.
   - Blur quarantine: restricts blurs to the floating top bar to keep mobile scrolling locked at 60 to 120 FPS.
   - Light-catching 1px hairline borders for crisp depth without heavy drop shadows.

4. **Optical Typography & Proportions**:
   - Size-specific optical tracking: negative letter-spacing on display headers, neutral on body, positive on small captions.
   - Inverse optical leading: tight line height on headings, comfortable line height on body copy.
   - Platform system font foundations for instant rendering with zero layout shift.

5. **Midnight Monochrome Contrast System**:
   - Pitch-black obsidian dark mode paired with crisp hairline borders.
   - High-contrast, clean light mode.
   - Zero-flash theme persistence script to stop light and dark flashes on page load.
   - Keyboard-friendly tactile theme toggle helper.

6. **Command Palette & Global Search**:
   - Quick search and action palette triggered with `Cmd+K` or `Ctrl+K`.
   - Focuses cleanly without causing page scroll jumps (`preventScroll: true`).
   - Renders through a document portal so ancestor styles never clip or blur it.
   - Keeps mobile headers uncluttered by hiding keyboard shortcut badges on phone screens.

7. **Accessibility & Multi-Signal Adaptation**:
   - Replaces vestibular spring motion with subtle opacity cross-fades for reduced motion.
   - Drops blurs to solid opaque surfaces for reduced transparency.
   - Strengthens hairline borders for increased contrast settings.

8. **Typography, Punctuation, & Copy Hygiene**:
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
