#  Design System — jumia-a11y

> The single source of truth for all visual decisions.
> Every color, font size, and spacing value here is **WCAG 2.1 AA approved**.
> Designers and developers must use ONLY these values.

---

##  Color Palette

All color pairs below meet **minimum AA contrast ratio (4.5:1 for text, 3:1 for UI elements)**.

### Primary Colors (Jumia-inspired, accessibility-adjusted)

| Token | Hex | Usage | Contrast on White |
|---|---|---|---|
| `--color-primary` | `#C8001E` | Primary buttons, links, badges | 5.9:1 ✅ |
| `--color-primary-dark` | `#9B0016` | Hover state for primary | 8.2:1 ✅ |
| `--color-primary-light` | `#FFE5E9` | Backgrounds, highlights | — |

### Neutral Colors

| Token | Hex | Usage | Contrast on White |
|---|---|---|---|
| `--color-text-primary` | `#1A1A1A` | Body text, headings | 16.1:1 ✅ |
| `--color-text-secondary` | `#4A4A4A` | Supporting text, labels | 9.7:1 ✅ |
| `--color-text-muted` | `#767676` | Placeholders, captions | 4.5:1 ✅ AA minimum |
| `--color-bg-white` | `#FFFFFF` | Page background | — |
| `--color-bg-light` | `#F5F5F5` | Card backgrounds, sections | — |
| `--color-border` | `#C0C0C0` | Input borders, dividers | 3.0:1 ✅ (UI) |

### Semantic / Status Colors

| Token | Hex | Usage | Contrast on White |
|---|---|---|---|
| `--color-success` | `#1A7A3C` | Success messages, in-stock | 5.2:1 ✅ |
| `--color-error` | `#C8001E` | Error messages, out-of-stock | 5.9:1 ✅ |
| `--color-warning` | `#7A5200` | Warning states | 5.0:1 ✅ |
| `--color-info` | `#005A9E` | Info badges, tooltips | 7.1:1 ✅ |
| `--color-focus-ring` | `#005A9E` | Keyboard focus outline | 7.1:1 ✅ |

> ⚠️ **Designer note:** Never use color alone to communicate status. Always pair with an icon or text label (e.g., don't just turn a border red — add "This field is required" text too).

---

##  Typography Scale

Base font size: **16px (1rem)** — never go below this for body text.

| Token | Size | Weight | Usage |
|---|---|---|---|
| `--text-xs` | 12px / 0.75rem | 400 | Legal text, fine print only |
| `--text-sm` | 14px / 0.875rem | 400 | Secondary labels, metadata |
| `--text-base` | 16px / 1rem | 400 | Body text |
| `--text-lg` | 18px / 1.125rem | 400 | Lead text, product descriptions |
| `--text-xl` | 20px / 1.25rem | 600 | Section headings (h3) |
| `--text-2xl` | 24px / 1.5rem | 700 | Page subheadings (h2) |
| `--text-3xl` | 30px / 1.875rem | 700 | Product title (h1) |
| `--text-price` | 24px / 1.5rem | 700 | Product price |

**Rules:**
- Use `rem` units, never `px` for font sizes (allows browser text resize to work)
- Line height minimum: `1.5` for body text (WCAG 1.4.8)
- Letter spacing: `0.12em` minimum for body text
- Never justify text (`text-align: justify`) — causes uneven word spacing

---

##  Spacing Scale

Based on a 4px base unit:

| Token | Value | Usage |
|---|---|---|
| `--space-1` | 4px | Tight padding (icon gaps) |
| `--space-2` | 8px | Small gaps |
| `--space-3` | 12px | Input padding |
| `--space-4` | 16px | Default padding |
| `--space-5` | 20px | Card padding |
| `--space-6` | 24px | Section gaps |
| `--space-8` | 32px | Large sections |
| `--space-12` | 48px | Page sections |

---

##  Interactive Element Sizes

| Element | Minimum Size | Reason |
|---|---|---|
| Buttons | 44px × 44px | WCAG 2.5.5 Target Size |
| Icon buttons | 44px × 44px | WCAG 2.5.5 |
| Checkboxes / Radios | 24px × 24px | Usability |
| Links (touch) | 44px hit area | Mobile accessibility |

---

##  Focus Indicator

All focusable elements must have this focus style (or equivalent):

```css
:focus-visible {
  outline: 3px solid var(--color-focus-ring); /* #005A9E */
  outline-offset: 2px;
  border-radius: 2px;
}

/* Remove default outline only when providing custom */
:focus:not(:focus-visible) {
  outline: none;
}
```

> ⚠️ **Never use** `outline: none` or `outline: 0` without providing a visible replacement.

---

##  Tailwind Config Tokens

Add to `tailwind.config.ts` to use design tokens as Tailwind classes:

```typescript
import type { Config } from 'tailwindcss'

const config: Config = {
  theme: {
    extend: {
      colors: {
        primary: {
          DEFAULT: '#C8001E',
          dark: '#9B0016',
          light: '#FFE5E9',
        },
        text: {
          primary: '#1A1A1A',
          secondary: '#4A4A4A',
          muted: '#767676',
        },
        status: {
          success: '#1A7A3C',
          error: '#C8001E',
          warning: '#7A5200',
          info: '#005A9E',
        },
        focus: '#005A9E',
      },
      fontSize: {
        'price': ['1.5rem', { fontWeight: '700', lineHeight: '1.3' }],
      },
      minHeight: {
        'touch': '44px',
      },
      minWidth: {
        'touch': '44px',
      },
    },
  },
}

export default config
```

---

##  Designer Handoff Checklist

Before handing assets to developers, confirm:

- [ ] All text/background color pairs checked with Vispero contrast checker
- [ ] No information conveyed by color alone
- [ ] All icons have a visible text label or tooltip
- [ ] Button and input sizes meet 44×44px minimum
- [ ] Focus state designed for every interactive component
- [ ] Before/after comparison screens exported as PNG into `docs/design-assets/`
- [ ] Accessible color palette exported as a Figma/CSS file
