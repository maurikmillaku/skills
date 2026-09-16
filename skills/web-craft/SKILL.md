---
name: web-craft
description: Elevate any existing website to world-class software standards. Complete, self-contained system for sub-second speed, platform and touch defect eradication, fluid spring physics, gesture momentum, optical typography, midnight monochrome contrast, command palette search, and typography hygiene. Single-install skill that transforms an ordinary website into high-craft software.
---

# Web Craft Standards

## Initial Response

When this skill is first invoked without a specific question, respond only with:

> I am ready to elevate your website to world-class craft, speed, and tactile polish.

Do not provide any other information until the user asks a question or shares their code.

---

## Operating Posture

You are a senior design engineer and performance architect with an uncompromising standard for software craft. You evaluate codebases by inspecting real code, testing against touch hardware realities, and refusing to rely on desktop browser emulation.

You understand that making an application or website feel extraordinary does not require heavy runtime libraries, bloated frameworks, or endless redesign cycles. It requires discipline across eight self-contained pillars:

1. **Touch & Platform Defect Eradication**: Eliminating the subtle platform glitches that make a web app feel cheap on a phone.
2. **Fluid Physics, Springs, & Gestures**: Instant physical response on touch down, critically damped springs, velocity handoffs, interruptibility, and rubber-banding.
3. **Materials, Translucency, & Depth**: Floating functional chrome, blur quarantine to preserve 60 to 120 FPS, and hairline light-catching borders.
4. **Optical Typography & Proportions**: Size-specific tracking tables, inverse leading, system font foundations, and layout stability.
5. **Midnight Monochrome Contrast Architecture**: High-contrast dark and light modes, hairline borders, and zero-flash theme persistence.
6. **Command Palette & Global Search**: Instant keyboard navigation (`Cmd+K`), portal dialogs, scroll-safe focus, and uncluttered mobile headers.
7. **Accessibility & Multi-Signal Adaptation**: Graceful fallbacks for reduced motion, reduced transparency, and increased contrast.
8. **Typography, Punctuation, & Copy Hygiene**: Zero em-dashes, zero directional UI arrows, and minimal, direct, human communication.

This skill is completely self-contained. Anyone using this skill has every rule, formula, diagnostic check, and code snippet needed to upgrade their website without installing secondary packages or skills.

---

## The Master Diagnostic Table

When evaluating any website, audit against this symptom table to identify defects and apply the exact production fix:

| Symptom | Root Cause | Exact Production Fix |
| :--- | :--- | :--- |
| **Hover state stuck after tap on phone** | Desktop `:hover` styles applied to touchscreens | Gate every hover style behind `@media (hover: hover) and (pointer: fine)`. Move touch feedback to `:active`. |
| **Blue or gray box flash on tap** | Browser default touch highlight overlay | Set `-webkit-tap-highlight-color: transparent` globally on `html`. |
| **Layout has wrong height on mobile** | Sizing with `100vh`, which ignores the dynamic browser URL bar | Use `100dvh` for app shells and drawers, and `100svh` for hero sections. |
| **Page zooms into input on focus** | Form input font size is smaller than 16px on mobile Safari | Set `font-size: 16px !important` on `input, textarea, select`. Never disable user scaling. |
| **Buttons feel delayed or dead to press** | Click handlers waiting for mouse-up and 300ms double-tap delay | Add `touch-action: manipulation` and an `:active` state with `transform: scale(0.97)`. |
| **Pull-to-refresh hijacks scroll** | Unconstrained page overscroll competing with browser gestures | Apply `overscroll-behavior-y: contain` to scroll containers or `none` where appropriate. |
| **Content cut off by phone notch** | Viewport stopping short of device display edges | Add `viewport-fit=cover` in meta tag and use `env(safe-area-inset-top)` and `env(safe-area-inset-bottom)`. |
| **Long-press selects button text** | Missing text-selection prevention on interactive elements | Apply `user-select: none; -webkit-user-select: none` to buttons, tabs, and interactive pills. |
| **Status bar color looks mismatched** | Browser top bar color sampler sampling page gradients | Provide matching `meta name="theme-color"` for light and dark modes, and keep page canvas clean. |
| **Animation feels abrupt or robotic** | Linear or generic cubic-bezier easing with arbitrary durations | Switch to critically damped springs (damping 1.0, response 0.3 to 0.4s) or fast settle curves. |
| **Gesture freezes when finger releases** | Snapping to nearest boundary without considering velocity | Hand off gesture velocity to spring and use momentum projection to calculate landing endpoint. |
| **Boundary stop feels jarring** | Hard clamping at scroll or swipe limits | Apply rubber-banding progressive resistance formula past the boundary. |
| **Headings feel loose; body text tight** | Uniform letter-spacing across all font sizes | Apply optical tracking: negative letter-spacing on large display type, zero on body, positive on small captions. |
| **Command menu jumps page scroll on open** | `input.focus()` causing the browser to auto-scroll to the input | Call `input.focus({ preventScroll: true })`. |
| **Modal inherits parent blur or transforms** | Dialog nested inside an ancestor with `backdrop-filter` or `transform` | Teleport the modal to `document.body` using a React Portal. |
| **Mobile header crowded with key badges** | Displaying `Cmd+K` or `Ctrl+K` badges on phone screens | Hide the shortcut badge on mobile viewports (< 641px) using CSS media queries. |
| **Dark mode looks muddy or washed out** | Low-contrast generic grays (`#222`, `#333`) | Use deep obsidian black (`#000000` or `#050505`) with 1px hairline borders (`rgba(255, 255, 255, 0.08)`). |
| **Mobile scroll stutters and drops frames** | Repeating `backdrop-filter: blur()` forcing offscreen GPU compositing | Remove blurs from cards and list items. Keep blurs strictly on the single floating top bar. |
| **Transitions feel laggy on budget phones** | Animating layout properties (`width`, `height`, `top`, `margin`) | Animate strictly GPU-composited properties: `transform` and `opacity`. |
| **Page shifts when custom fonts load** | Unmatched fallback font metrics triggering layout shift (CLS) | Self-host fonts, use `font-display: swap`, and define size-adjust fallbacks. |
| **Copy sounds robotic or corporate** | AI boilerplate and buzzwords ("delve", "seamless", "game-changing") | Rewrite in direct, grounded, human language focused on real outcomes. |
| **UI cluttered with directional arrows** | Using decorative symbols as crutches for affordance | Remove all directional arrows. Rely on clean typography, spacing, and contrast. |
| **Punctuation clutter from em-dashes** | Overusing em-dash characters in copy and headers | Replace em-dashes with commas, parentheses, or concise sentence breaks. |

---

## Pillar 1: Touch & Platform Defect Eradication

Web apps feel like second-class software on phones when they ignore platform realities. These baseline rules fix touch defects at the platform level:

### 1. Global Touch Hygiene Baseline
Inject this baseline into the global stylesheet of every project:

```css
html {
  /* Eliminate the gray and blue tap highlight box on iOS and Android */
  -webkit-tap-highlight-color: transparent;
  
  /* Smooth scrolling for anchor links */
  scroll-behavior: smooth;
  
  /* Prevent horizontal page drift */
  overflow-x: hidden;
}

/* Enforce 16px minimum on touch inputs to prevent iOS Safari auto-zoom */
input,
textarea,
select {
  font-size: 16px !important;
}

/* Eliminate 300ms tap delay and prevent long-press text selection on UI controls */
button,
a,
[role="button"],
.tappable {
  touch-action: manipulation;
  user-select: none;
  -webkit-user-select: none;
}
```

### 2. The Sticky Hover Rule
Touchscreens do not have a cursor hovering over elements. When a mobile user taps an element with `:hover` styles, the browser fakes hover by locking the element in its hover state until another element is tapped.

Always isolate hover styles behind a capability query:

```css
/* CORRECT: Only devices with a fine pointer (mouse, trackpad) receive hover states */
@media (hover: hover) and (pointer: fine) {
  .button:hover {
    background-color: var(--surface-hover);
    transform: translateY(-1px);
    border-color: var(--border-strong);
  }
}

/* Touch feedback belongs strictly on active press */
.button:active {
  transform: scale(0.97);
  background-color: var(--surface-active);
}
```

### 3. Dynamic Viewport Heights
`100vh` calculates viewport height based on the browser chrome being completely hidden. When the mobile URL bar is visible, `100vh` overflows the screen, pushing bottom elements off-screen.

```css
/* App shells, drawers, and overlays that dynamically track browser chrome */
.app-shell,
.modal-overlay {
  height: 100dvh;
}

/* Hero sections and landing screens that must never be cut off */
.hero-section {
  min-height: 100svh;
}
```

### 4. Safe Areas & Display Notches
Ensure full-bleed layouts respect notches and home indicator bars:

```html
<!-- In HTML head: enable full-bleed viewport -->
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
```

```css
/* Apply safe area padding to fixed topbars and bottom navigation */
.header {
  padding-top: max(1rem, env(safe-area-inset-top));
}

.bottom-bar {
  padding-bottom: max(1rem, env(safe-area-inset-bottom));
}
```

### 5. Status Bar & Canvas Color Coordination
Mobile browsers (like Safari) sample the top of the canvas to color the device status bar. Conflicting full-page background gradients or mismatched theme meta tags cause disjointed status bars.

```html
<!-- In HTML head: specify matching theme colors for both modes -->
<meta name="theme-color" content="#ffffff" media="(prefers-color-scheme: light)">
<meta name="theme-color" content="#000000" media="(prefers-color-scheme: dark)">
```

Keep the root `background-color` solid so the color sampler matches the canvas seamlessly.

---

## Pillar 2: Fluid Physics, Springs, & Gestures

Great software feels physical. When you touch an element on a well-built system, it reacts the millisecond your finger touches down, carries momentum, and can be redirected mid-motion without jumping.

### 1. Instant Active Response
Feedback on mouse-up reads as input lag. Every button, card, and interactive row must compress immediately on press:

```css
/* Standard tactile button */
.btn-tactile {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  font-weight: 500;
  border-radius: 8px;
  cursor: pointer;
  touch-action: manipulation;
  user-select: none;
  -webkit-user-select: none;
  
  /* Hardware-accelerated transition */
  transition: transform 140ms cubic-bezier(0.16, 1, 0.3, 1),
              background-color 160ms ease-out,
              border-color 160ms ease-out,
              opacity 140ms ease-out;
}

/* Subtle lift on desktop hover */
@media (hover: hover) and (pointer: fine) {
  .btn-tactile:hover {
    transform: translateY(-1px);
  }
}

/* Physical compression on active press */
.btn-tactile:active {
  transform: scale(0.96);
  opacity: 0.92;
}
```

### 2. Spring Parameter Architecture
A pre-scripted, fixed-duration animation cannot respond naturally to new input. A spring can: new input simply changes the target, and motion stays continuous.

Think in two designer-friendly parameters rather than raw mass and stiffness:
- **Damping Ratio**: Controls overshoot and bounce.
  - `1.0`: Critically damped. No overshoot, smooth graceful settle. Use as the rock-solid default across all standard UI.
  - `0.8`: Under-damped. Slight bounce. Reserve strictly for momentum-driven gestures (a flick, throw, or drag release). Never put bounce on a menu that simply opened.
- **Response**: How quickly the value reaches the target, in seconds. Lower means snappier. Standard UI uses `0.3s` to `0.4s`.

```javascript
// Damping and Response Reference Table
// Standard reposition / popover: damping 1.0, response 0.35s
// Sheet / drawer swipe: damping 0.8, response 0.30s
// Card dismiss flick: damping 0.85, response 0.28s
```

### 3. Direct Manipulation & Grab Offset
When dragging or swiping, content must remain glued 1:1 with the pointer. Snapping to the center of an element on grab breaks the physical illusion.

```javascript
element.addEventListener('pointerdown', (event) => {
  element.setPointerCapture(event.pointerId);
  const grabOffsetY = event.clientY - element.getBoundingClientRect().top;
  // Track position history and timestamps across pointermove to calculate release velocity
});
```

### 4. Interruptibility & Presentation Values
Never lock out user input during an animation. An active transition must be interruptible at any millisecond.
- Always read the element's current on-screen computed transform (presentation value) when interrupted, and start the new animation from there. Starting from the target value causes a visible frame skip.
- Decompose 2D motion into independent X and Y springs so varying horizontal and vertical speeds do not desynchronize.

### 5. Velocity Handoff
When a swipe or drag ends, the trailing animation must start at the finger's exact release velocity so there is zero seam between dragging and coasting:

```javascript
// Normalized relative velocity formula
// relativeVelocity = gestureVelocity / (targetValue - currentValue)
```

### 6. Momentum Projection Formula
Do not snap to the nearest boundary based solely on release coordinates. Project the resting endpoint using velocity decay, exactly like native scroll:

```javascript
function projectMomentum(initialVelocity, decelerationRate = 0.998) {
  // initialVelocity in pixels per second
  return (initialVelocity / 1000) * decelerationRate / (1 - decelerationRate);
}

const projectedEndpoint = currentPosition + projectMomentum(releaseVelocity);
// Select the nearest snap target based on projectedEndpoint, then hand off velocity
```

### 7. Rubber-Banding Boundary Resistance
At boundaries, resist progressively rather than hitting a solid stop. A hard stop reads as frozen; progressive resistance reads as responsive:

```javascript
function calculateRubberBand(overshoot, dimension, constant = 0.55) {
  return (overshoot * dimension * constant) / (dimension + constant * Math.abs(overshoot));
}
```

### 8. GPU Compositing Discipline
Never animate properties that trigger browser layout recalculations (`width`, `height`, `top`, `left`, `margin`, `padding`). Animate exclusively `transform` and `opacity`.

---

## Pillar 3: Materials, Translucency, & Depth

Translucent materials provide a functional, floating layer that creates visual structure without stealing attention.

### 1. The Blur Quarantine Rule
`backdrop-filter: blur(...)` requires off-screen GPU compositing buffers. Stacking blurs kills mobile performance.
- **Permitted**: Exactly one floating top bar or one active modal backdrop.
- **Forbidden**: Blurs on repeating card grids, list rows, badges, or buttons.
- **Fix**: Use opaque or semi-opaque solid surfaces (`var(--surface)`) paired with 1px hairline borders.

### 2. Floating Chrome Specifications
```css
.floating-header {
  position: sticky;
  top: 0;
  z-index: 40;
  background-color: rgba(255, 255, 255, 0.75);
  backdrop-filter: blur(16px) saturate(180%);
  -webkit-backdrop-filter: blur(16px) saturate(180%);
  border-bottom: 1px solid var(--border-soft);
}

[data-theme="dark"] .floating-header {
  background-color: rgba(0, 0, 0, 0.72);
  border-bottom: 1px solid var(--border-soft);
}
```

### 3. Light-Catching Hairline Borders
High-craft surfaces achieve depth without heavy drop shadows by catching light at their borders:
- Dark mode: `border: 1px solid rgba(255, 255, 255, 0.08)`
- Light mode: `border: 1px solid rgba(0, 0, 0, 0.08)`

---

## Pillar 4: Optical Typography & Proportions

Type changes optical proportions as size changes. Great software tunes tracking and leading deliberately.

### 1. Optical Tracking (Letter-Spacing)
- **Large Display Headings (32px+)**: Letters appear spaced too far apart as size scales up. Apply negative tracking (`-0.02em` to `-0.03em`).
- **Body Copy (15px to 18px)**: Keep tracking neutral (`0` to `-0.01em`).
- **Small Captions & Badges (11px to 13px)**: Letters crowd together. Apply positive tracking (`+0.01em` to `+0.03em`).

### 2. Optical Leading (Line-Height)
Line height tracks font size inversely:
- **Display Headings**: Tight leading (`1.05` to `1.15`) prevents headers from looking loose and fragmented.
- **Body Text**: Comfortable leading (`1.5` to `1.65`) prevents eye fatigue across paragraphs.

### 3. Platform System Font Foundations
Default to system font stacks before downloading custom web fonts. System fonts ship built-in optical sizing tables and eliminate layout shifts (CLS):

```css
:root {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
}
```

---

## Pillar 5: Midnight Monochrome Contrast Architecture

Muddy grays make interfaces look washed out. High-craft software uses calibrated monochrome: deep obsidian dark mode, crisp clean light mode, and hairline definition.

### 1. Unified Design Tokens
Drop these CSS variables into the root stylesheet:

```css
:root {
  /* Light Mode Base */
  --bg: #ffffff;
  --surface: #fafafa;
  --surface-alt: #f4f4f5;
  --surface-active: #e4e4e7;
  
  /* Ink Hierarchy */
  --ink: #111111;
  --ink-soft: #555555;
  --ink-muted: #888888;
  
  /* Hairline Borders */
  --border-soft: rgba(0, 0, 0, 0.08);
  --border-strong: rgba(0, 0, 0, 0.16);
  
  /* Shadows */
  --shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.05);
  --shadow-md: 0 4px 12px rgba(0, 0, 0, 0.08);
}

[data-theme="dark"] {
  /* Midnight Dark Base */
  --bg: #000000;
  --surface: #0a0a0a;
  --surface-alt: #121212;
  --surface-active: #1a1a1a;
  
  /* Ink Hierarchy */
  --ink: #ededed;
  --ink-soft: #a1a1a6;
  --ink-muted: #71717a;
  
  /* Hairline Borders */
  --border-soft: rgba(255, 255, 255, 0.08);
  --border-strong: rgba(255, 255, 255, 0.18);
  
  /* Shadows */
  --shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.4);
  --shadow-md: 0 4px 20px rgba(0, 0, 0, 0.6);
}
```

### 2. Zero-Flash Theme Persistence Script
Inject this minimal blocking script at the very top of `<head>` to prevent white/black flash:

```html
<script>
  (function() {
    try {
      var saved = localStorage.getItem('theme');
      var systemDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
      if (saved === 'dark' || (!saved && systemDark)) {
        document.documentElement.setAttribute('data-theme', 'dark');
      } else {
        document.documentElement.setAttribute('data-theme', 'light');
      }
    } catch (e) {}
  })();
</script>
```

### 3. Tactile Theme Toggle Helper
```typescript
export function toggleTheme(): 'light' | 'dark' {
  const current = document.documentElement.getAttribute('data-theme');
  const next = current === 'dark' ? 'light' : 'dark';
  document.documentElement.setAttribute('data-theme', next);
  try {
    localStorage.setItem('theme', next);
  } catch (e) {}
  return next;
}
```

---

## Pillar 6: Command Palette & Global Search Pattern

A command palette gives immediate keyboard access to navigation and core actions without digging through menus.

### 1. Key Implementation Rules
1. **Focus Without Scroll Jump**: Always invoke `input.focus({ preventScroll: true })`. Calling standard `focus()` causes browsers to scroll the document down to where the input sits.
2. **React Portal to Document Root**: Render dialogs inside `document.body` via `createPortal`. Nesting a dialog inside page sections causes z-index clipping and blur inheritance bugs.
3. **Uncluttered Mobile Header**: Never show keyboard shortcut badges (`Cmd+K` or `Ctrl+K`) on mobile viewports. Phones do not have Command or Control keys. Hide the badge on viewports below 641px width.
4. **Instant Keyboard Navigation**: Arrow Up, Arrow Down, Enter to execute, Escape to dismiss.

### 2. Mobile Responsive Trigger Styling
```css
.cmdk-trigger {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 34px;
  height: 34px;
  border-radius: 50%;
  border: 1px solid var(--border-soft);
  background-color: var(--surface);
  color: var(--ink-soft);
  font-family: monospace;
  font-size: 0.72rem;
  font-weight: 600;
  cursor: pointer;
  touch-action: manipulation;
  user-select: none;
  -webkit-user-select: none;
  transition: transform 120ms ease-out, background-color 160ms ease-out;
}

.cmdk-trigger:active {
  transform: scale(0.92);
}

/* Eliminate clutter on mobile phones */
@media (max-width: 640px) {
  .cmdk-trigger {
    display: none !important;
  }
}
```

---

## Pillar 7: Accessibility & Multi-Signal Adaptation

World-class software adapts to user capabilities and system preferences without losing functional feedback.

### 1. Reduced Motion
Reduced motion does not mean zero feedback; it means gentle, non-vestibular equivalents:
```css
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
  
  /* Replace spring slides with subtle opacity cross-fades */
  .modal-overlay,
  .dialog-content {
    transition: opacity 160ms ease-out !important;
    transform: none !important;
  }
}
```

### 2. Reduced Transparency & High Contrast
```css
@media (prefers-reduced-transparency: reduce) {
  .floating-header,
  .modal-overlay {
    backdrop-filter: none !important;
    -webkit-backdrop-filter: none !important;
    background-color: var(--bg) !important;
  }
}

@media (prefers-contrast: more) {
  :root {
    --border-soft: rgba(0, 0, 0, 0.35);
  }
  [data-theme="dark"] {
    --border-soft: rgba(255, 255, 255, 0.45);
  }
}
```

---

## Pillar 8: Typography, Punctuation, & Copy Hygiene

World-class software communicates with clarity, restraint, and confidence.

### 1. Punctuation Hygiene
- **Never use em-dashes (`—`)**: They clutter sentences and look like AI-generated text. Use standard commas, parentheses, or clean sentence breaks instead.

### 2. Directional Restraint
- **Never use UI arrows (`->`, `<-`, `ArrowRight`, `ArrowLeft`)**: Rely on clean typography, contrast, and spacing to indicate interactive affordance. Clean text on a button or link is sufficient.

### 3. Anti-AI Copywriting Principles
- Strip out marketing buzzwords and filler phrases ("delve", "seamlessly", "cutting-edge", "game-changing", "bespoke", "revolutionary").
- Write in direct, grounded language. Focus on real outcomes: load speed, mobile ergonomics, clear pricing, direct contact.
- Avoid decorative badges ("Interactive Showcase", "Cryptographic Experience"). If an element is interactive, let the user interact with it directly.

---

## Codebase Audit & Execution Protocol

When instructed to audit or elevate a website, follow this methodical execution workflow:

### Step 1: Scan for Platform Defect Tells
1. Check global CSS for `-webkit-tap-highlight-color: transparent`.
2. Check for unguarded `:hover` rules that trigger sticky hover on mobile.
3. Check input elements for font sizes below 16px.
4. Check for `100vh` usage on elements that should use `100dvh` or `100svh`.
5. Check if buttons and tappable elements have `user-select: none` and `touch-action: manipulation`.

### Step 2: Audit Compositing, Springs, & Gestures
1. Search stylesheets for transitions on `width`, `height`, `top`, `left`, `margin`, or `padding`.
2. Verify interactive elements have instant `:active` scale compression.
3. Ensure gestures calculate velocity handoff and momentum projection instead of dead stops.
4. Verify boundary resistance uses progressive rubber-banding.

### Step 3: Inspect Translucency & Optical Type
1. Quarantine blurs: ensure blurs are restricted to a single navigation bar.
2. Check typography tracking: negative tracking on large display text, neutral on body.
3. Verify line heights: tight on display headings, comfortable on body copy.

### Step 4: Inspect Theme & Contrast Palette
1. Check dark mode background color. Replace washed out grays with deep obsidian black (`#000000` or `#050505`).
2. Verify hairline borders (`rgba(255, 255, 255, 0.08)` in dark, `rgba(0, 0, 0, 0.08)` in light).
3. Ensure theme selection persists across reloads with zero white/black flash.

### Step 5: Refine Navigation & Search
1. If a command palette exists, verify `preventScroll: true` is passed to input focus.
2. Ensure the palette renders via a portal at `document.body`.
3. Verify that shortcut badges like `Cmd+K` are hidden on mobile viewports (< 641px) to prevent header clutter.

### Step 6: Clean Typography & Copy
1. Search all copy for em-dash characters (`—`) and replace with commas, parentheses, or clean breaks.
2. Search buttons, links, and headers for arrow characters (`->`, `<-`, `&rarr;`) and remove them.
3. Strip generic corporate buzzwords and replace with clear, human phrasing.

### Step 7: Output Summary
Report your findings and modifications in a concise table:

| Area | File Modified | Defect Identified | Action Taken |
| :--- | :--- | :--- | :--- |
| Mobile Touch | `src/styles/globals.css` | Tap highlight flash on phone | Added `-webkit-tap-highlight-color: transparent` |
| Fluid Physics | `src/components/Card.tsx` | Drag gesture stopped hard at boundary | Implemented rubber-band resistance formula |
| Tactile Motion | `src/components/Button.tsx` | Sluggish click response | Added `:active` scale compression (0.97) |
| Optical Type | `src/styles/typography.css` | Loose display text tracking | Applied `-0.025em` tracking to headings |
| Mobile Header | `src/components/Header.css` | `Cmd+K` badge crowding mobile navigation | Hidden shortcut badge on screens < 641px |
| Typography | `src/content/about.md` | Em-dashes and arrow symbols | Cleaned punctuation and removed UI arrows |
