# 🔍 WCAG 2.1 Audit Checklist — Jumia Product Page

> Run this checklist before (baseline audit) and after (final review) implementation.
> Target: **WCAG 2.1 Level AA**

---

## Tools to Use
- [axe DevTools](https://www.deque.com/axe/devtools/) — Chrome extension
- [WAVE](https://wave.webaim.org/) — web audit tool
- [NVDA](https://www.nvaccess.org/) — free screen reader (Windows)
- [VoiceOver](https://support.apple.com/guide/voiceover/) — built-in (Mac/iOS)
- [Vispero Contrast Checker](https://vispero.com/color-contrast-checker/)
- Keyboard-only navigation test (unplug/ignore mouse)

---

## P — Perceivable

### Text Alternatives
- [ ] Every non-decorative image has a descriptive `alt` attribute
- [ ] Decorative images have `alt=""`
- [ ] Icon-only buttons have `aria-label` or visually hidden text
- [ ] Product thumbnails have meaningful alt text (e.g., "iPhone 15 Pro — Black, front view")

### Time-Based Media
- [ ] Any video has captions or a transcript
- [ ] No autoplay audio without user control

### Adaptable
- [ ] Page structure makes sense when CSS is disabled
- [ ] Reading order is logical
- [ ] No reliance on color alone to convey info (e.g., "fields in red are required" — add text too)

### Distinguishable
- [ ] Normal text contrast ≥ 4.5:1
- [ ] Large text (18pt+ or 14pt bold) contrast ≥ 3:1
- [ ] UI components (buttons, inputs) contrast ≥ 3:1 against background
- [ ] Text resizes to 200% without horizontal scroll or lost content
- [ ] No text embedded in images (except logos)
- [ ] Page is usable at 400% zoom

---

## O — Operable

### Keyboard Accessible
- [ ] All functionality available via keyboard alone
- [ ] No keyboard traps (user can always Tab out of any component)
- [ ] Dropdowns, modals, and custom widgets are keyboard-navigable
- [ ] Add-to-cart, wishlist, quantity buttons all reachable by Tab

### Enough Time
- [ ] No time limits, OR user can extend/turn off timers
- [ ] Auto-playing carousels can be paused

### Seizures & Physical Reactions
- [ ] No content flashes more than 3 times per second

### Navigable
- [ ] Skip navigation link present and visible on focus
- [ ] Page has a descriptive `<title>`
- [ ] Focus order is logical (top-to-bottom, left-to-right)
- [ ] All links have descriptive text (not "click here" or "read more")
- [ ] Focus is visible at all times (`:focus-visible` style applied)

---

## U — Understandable

### Readable
- [ ] `<html lang="en">` set on the page
- [ ] Unusual words or abbreviations are explained

### Predictable
- [ ] Pages behave consistently across the site
- [ ] Navigation is in the same place on each page
- [ ] No unexpected context changes on focus or input

### Input Assistance
- [ ] All form inputs have associated `<label>` elements
- [ ] Error messages are descriptive and suggest corrections
- [ ] Required fields are clearly identified
- [ ] `autocomplete` attributes used where appropriate
- [ ] Input purpose can be programmatically determined

---

## R — Robust

### Compatible
- [ ] Valid HTML (run through [W3C Validator](https://validator.w3.org/))
- [ ] No duplicate IDs
- [ ] All interactive elements have accessible names
- [ ] ARIA is used correctly — roles, states, properties
- [ ] `aria-live` regions used for dynamic content updates (cart count, toast messages)
- [ ] Works with NVDA + Chrome and VoiceOver + Safari

---

## 📊 Audit Score Template

Fill this in before and after implementation:

| Area | Issues Found (Before) | Issues Fixed (After) | Status |
|---|---|---|---|
| Perceivable | | | 🔴 / 🟡 / 🟢 |
| Operable | | | 🔴 / 🟡 / 🟢 |
| Understandable | | | 🔴 / 🟡 / 🟢 |
| Robust | | | 🔴 / 🟡 / 🟢 |

> 🔴 Not started | 🟡 In progress | 🟢 Complete
