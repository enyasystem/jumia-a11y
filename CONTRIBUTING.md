#  Contributing Guide — jumia-a11y

> Read this before writing a single line of code.

---

## 🌿 Branch Rules

| Branch | Purpose |
|---|---|
| `main` | Final, submission-ready code only |
| `develop` | Integration branch — all PRs go here |
| `feature/*` | Your working branch |

**Never push directly to `main` or `develop`.** Always work on your feature branch and open a PR.

---

##  Your Branches

| Team Member | Branch |
|---|---|
| Elvis  | `feature/robust-aria-semantic` |
| Engr Tunde | `feature/operable-keyboard-nav` |
| Samson | `feature/perceivable-contrast-media` |
| Rachael | `feature/understandable-forms-labels` |
| David | Upload assets to `docs/design-assets/` via your branch |

---

##  Workflow (Do This Every Day)

```bash
# 1. Pull latest changes from develop before you start work
git checkout feature/your-branch
git pull origin develop

# 2. Do your work, then stage and commit
git add .
git commit -m "type: short description"

# 3. Push your branch
git push origin feature/your-branch

# 4. Open a Pull Request into develop on GitHub
```

---

##  Commit Message Format

Use this simple format:

```
type: short description of what you did
```

| Type | When to use |
|---|---|
| `feat` | Added something new |
| `fix` | Fixed a bug or accessibility issue |
| `a11y` | Accessibility-specific improvement |
| `style` | CSS / visual changes only |
| `docs` | Updated documentation |
| `test` | Added or updated tests |
| `refactor` | Code cleanup, no feature change |

**Examples:**
```
a11y: add aria-label to add-to-cart button
feat: implement focus trap for image modal
fix: correct tab order in product quantity selector
style: apply high-contrast color palette from design system
docs: update WCAG checklist with audit results
```

---

##  Pull Request Rules

1. **One PR per WCAG area** — don't mix concerns
2. **Title format:** `[WCAG-P] Fix image alt text on product gallery`
3. **Fill in the PR description** — what did you change and why?
4. **Tag Elvis as reviewer** on every PR
5. **PRs must pass** the axe-core test before merging (no new violations)
6. **No self-merging** — Elvis reviews and merges all PRs into `develop`

### PR Description Template

```markdown
## What this PR does
Brief description of changes made.

## WCAG Principle addressed
- [ ] Perceivable (P)
- [ ] Operable (O)
- [ ] Understandable (U)
- [ ] Robust (R)

## How to test
1. Run `npm run dev`
2. Open the product page
3. Tab through the page — verify focus indicators are visible
4. Run axe DevTools — confirm 0 new violations

## Screenshots (optional but appreciated)
Before | After
```

---

##  Code Standards

- Use **TypeScript** — no `any` types unless absolutely necessary
- Use **Tailwind** utility classes — no inline styles
- Every interactive element must have an accessible name (`aria-label`, `aria-labelledby`, or visible text)
- Never remove `:focus-visible` styles — if you override focus, add your own visible style
- Run `npm run lint` before opening a PR

---

##  Merge Deadlines

| Day | Action |
|---|---|
| Mar 8 (end of day) | All feature PRs open into `develop` |
| Mar 9 | Elvis reviews + merges, integration fixes |
| Mar 10 | Final PR from `develop` into `main` |
| Mar 11 | 🚨 Submission deadline |
