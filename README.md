# ♿ Jumia Product Page — WCAG Accessibility Redesign

> **FOASE Accessibility Challenge** | ALX Software Engineering × Creative Tech
> **Team Size:** 5 | **Deadline:** March 11, 2026

---

##  Project Goal

Audit and rebuild the [Jumia Product Page](https://https://www.jumia.com.ng/samsung-galaxy-z-fold-6-5g-7.6-12gb-512gb-rom-large-screen-404945551.html) to meet the **4 Principles of WCAG 2.1 (Level AA)**:

| Principle | Code | Focus |
|---|---|---|
| Perceivable | **P** | Alt text, contrast, captions, text resize |
| Operable | **O** | Keyboard nav, focus, skip links, timing |
| Understandable | **U** | Labels, error messages, predictable UI |
| Robust | **R** | Semantic HTML, ARIA, screen reader compat |

---

##  Tech Stack

| Layer | Tools |
|---|---|
| Frontend | React, TypeScript, Next.js |
| Design | Figma (high-contrast UI, accessible palette) |
| Accessibility | axe DevTools, WAVE, NVDA, ARIA |
| AI Assist | GitHub Copilot, atomica11y, Claude AI |

---

##  Project Structure

```
jumia-a11y/
├── public/
├── src/
│   ├── components/       # Accessible UI components
│   ├── pages/            # Next.js pages
│   ├── styles/           # High-contrast CSS/Tailwind
│   └── utils/            # a11y helpers (focus trap, ARIA utils)
├── docs/
│   ├── audit-report.md
│   ├── wcag-checklist.md
│   └── design-assets/
├── tests/
│   └── accessibility/    # axe-core automated tests
├── README.md
├── TASK_ASSIGNMENTS.md
└── CONTRIBUTING.md
```

---

##  Quick Start

```bash
git clone https://github.com/YOUR_ORG/jumia-a11y.git
cd jumia-a11y
npm install
npm run dev
```

---

##  Timeline

| Day | Date | Milestone |
|---|---|---|
| 1 | Mar 6 | Audit + Setup + Branch assignments |
| 2–3 | Mar 7–8 | WCAG fixes per team member |
| 4 | Mar 9 | Integration + Review |
| 5 | Mar 10 | Polish + Submit |
| ✅ | Mar 11 | **Deadline** |

---

## 🔗 Useful Resources

- [WCAG 2.1 Guidelines](https://www.w3.org/WAI/standards-guidelines/wcag/)
- [WAI-ARIA Patterns](https://www.w3.org/WAI/standards-guidelines/aria/)
- [W3C Tables Tutorial](https://www.w3.org/WAI/tutorials/tables/)
- [W3C Carousel Tutorial](https://www.w3.org/WAI/tutorials/carousels/)
- [Splide Accessible Carousel](https://splidejs.com/documents/)
- [Drag & Drop A11y Patterns](https://salesforce-ux.github.io/dnd-a11y-patterns/)
- [Atomica11y AI Tool](https://www.atomica11y.com/accessible-web/)
- [Vispero Contrast Checker](https://vispero.com/color-contrast-checker/)
- [Highcharts SVG Example](https://www.highcharts.com/demo/highcharts/spline-symbols)

---

##  Submission Checklist

- [ ] All WCAG P, O, U, R principles addressed
- [ ] Automated audit passes (axe / WAVE)
- [ ] Screen reader tested (NVDA / VoiceOver)
- [ ] Keyboard-only navigation works
- [ ] Designer before/after visuals included
- [ ] Team profiles ready for submission form
- [ ] Submitted via official FOASE form before **March 11**
