# 👥 Task Assignments — Jumia A11y Challenge

> **Deadline:** March 11, 2026 | **Team:** 5 members

---

## Elvis — Enya Elvis (Full-Stack)
**WCAG Principle: Robust (R)**

### Responsibilities
- [ ] Set up the GitHub repo, branch strategy, and project board
- [ ] Implement correct semantic HTML5 structure (`<main>`, `<nav>`, `<section>`, `<article>`, `<aside>`)
- [ ] Add ARIA roles, labels, and `aria-live` regions for dynamic content
- [ ] Ensure screen reader compatibility (test with NVDA / VoiceOver)
- [ ] Add `lang` attribute and proper document structure
- [ ] Implement skip-to-content link
- [ ] Handle meta tags for accessibility and SEO
- [ ] Review and merge all pull requests
- [ ] Coordinate final submission

**Branch:** `feature/robust-aria-semantic`

---

## Engr Tunde
**WCAG Principle: Operable (O)**

### Responsibilities
- [ ] Implement full keyboard navigation across the product page
- [ ] Add visible focus indicators (`:focus-visible` styles)
- [ ] Build skip navigation links
- [ ] Ensure all interactive elements are reachable via Tab/Shift+Tab
- [ ] Implement focus trapping for modals (cart, image viewer)
- [ ] Fix tab order to be logical and predictable
- [ ] Add `aria-expanded`, `aria-controls` to dropdowns and accordions
- [ ] Ensure no keyboard traps exist
- [ ] Implement pause/stop controls for any auto-playing content (carousels)

**Branch:** `feature/operable-keyboard-nav`

---

## Samson
**WCAG Principle: Perceivable (P)**

### Responsibilities
- [ ] Audit and fix all images — add meaningful `alt` text, mark decorative images with `alt=""`
- [ ] Fix color contrast to meet minimum AA ratio (4.5:1 for text, 3:1 for UI)
- [ ] Ensure text can resize up to 200% without loss of content
- [ ] Add captions or transcripts to any video/audio content
- [ ] Replace color-only cues with text or icons
- [ ] Implement responsive text scaling (avoid fixed `px` for font sizes)
- [ ] Add visible labels to all icon buttons (use `aria-label` or `<span class="sr-only">`)
- [ ] Test with browser zoom at 400%

**Branch:** `feature/perceivable-contrast-media`

---

## Rachael
**WCAG Principle: Understandable (U)**

### Responsibilities
- [ ] Add proper `<label>` elements to all form inputs (search, quantity, address)
- [ ] Implement descriptive error messages for form validation
- [ ] Ensure consistent navigation across pages
- [ ] Add `autocomplete` attributes to relevant form fields
- [ ] Make all instructions text-based (not just icon-only)
- [ ] Fix any jargon or unclear button labels (e.g., "Click here" → "Add iPhone 15 to cart")
- [ ] Ensure language of page is identified (`lang="en"`)
- [ ] Test and fix any unexpected behavior on page load or interaction

**Branch:** `feature/understandable-forms-labels`

---

## David
**Visual Design & Accessible Assets**

### Responsibilities
- [ ] Audit current Jumia product page design for visual accessibility issues
- [ ] Create **before/after** mockup showing accessibility improvements (this is key for winning!)
- [ ] Design a high-contrast color palette that meets WCAG AA
- [ ] Redesign icon-only buttons with visible text labels
- [ ] Create accessible image annotations for the dev team to implement
- [ ] Design accessible error state and empty state visuals
- [ ] Export all icons as SVGs with titles/descriptions
- [ ] Prepare design assets in `/docs/design-assets/` folder
- [ ] Create a one-page visual summary of changes for the submission

**Deliverable folder:** `docs/design-assets/`

---

##  Git Branch Strategy

```
main
├── develop              ← merge all features here first
│   ├── feature/robust-aria-semantic       (Elvis)
│   ├── feature/operable-keyboard-nav      (Engr Tunde)
│   ├── feature/perceivable-contrast-media (Samson)
│   └── feature/understandable-forms-labels (Rachael)
|   |__ docs/design-assets (David)
```

> ⚠️ No one pushes directly to `main`. All PRs go into `develop` first. Elvis reviews and merges.

---

## ✅ Daily Standup Template (Post in WhatsApp Group)

```
📅 Date:
✅ Done yesterday:
🔨 Doing today:
🚧 Blockers:
```

---

