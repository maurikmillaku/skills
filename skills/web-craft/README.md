# web-craft

An agent skill that elevates any website or web application to world-class software standards.

Inspired by the design and performance principles of **Apple WWDC design talks**, **Emil Kowalski's tactile physics**, **Paco Coursey's monochrome discipline**, and **Telegram's lightweight speed**.

---

## What It Audits & Fixes

1. **Sub-Second Compositing & Telegram-Style Speed**:
   - Eliminates GPU-choking stacked `backdrop-filter: blur()` from repeating content cards.
   - Enforces GPU-composited transitions (`transform` and `opacity` only).
2. **Platform & Mobile Defect Eradication**:
   - Kills sticky `:hover` states on touch devices.
   - Prevents iOS Safari input auto-zooming by enforcing 16px minimum font sizes.
   - Fixes anchor clipping with dynamic header headroom and clean URL hash hygiene (`history.replaceState`).
3. **Physical Tactile Response**:
   - Instant pointer-down press feedback (`scale(0.97)`).
   - Zero-latency command palette (`⌘K`) with view stability (`preventScroll: true`).
4. **Monochrome Palette & Restrained Copy**:
   - Midnight OLED contrast with subtle 1px border definition.
   - Elimination of em-dashes (`—`) and decorative UI arrows.
   - Anti-AI grounded copywriting.

---

## Installation

```bash
npx skills add Mauriki/web-craft
```

Or copy `SKILL.md` directly into your agent's `.agents/skills/web-craft/` directory.

---

## Author

**Maurik Millaku**
- Website: [maurikmillaku.com](https://maurikmillaku.com)
- GitHub: [@Mauriki](https://github.com/Mauriki)
- X (Twitter): [@maurikmillaku](https://x.com/maurikmillaku)
