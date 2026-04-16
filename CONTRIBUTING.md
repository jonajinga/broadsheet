# Contributing to Broadsheet

Thank you for your interest in contributing to Broadsheet. Every contribution matters — whether it is a bug report, a feature suggestion, a documentation improvement, or a pull request.

## Ways to Contribute

### Report a Bug

Open a [GitHub Issue](https://github.com/jonajinga/broadsheet/issues/new) with:
- What you expected to happen
- What actually happened
- Steps to reproduce
- Browser and OS version

### Suggest a Feature

Open a [GitHub Issue](https://github.com/jonajinga/broadsheet/issues/new) with the label `enhancement`. Describe:
- The problem the feature solves
- How you envision it working
- Whether you would be willing to implement it

### Submit a Pull Request

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Make your changes
4. Test locally (`npm start`)
5. Commit with a clear message (`git commit -m "Add: description of change"`)
6. Push to your fork (`git push origin feature/your-feature`)
7. Open a pull request against `main`

### Improve Documentation

Documentation improvements are always welcome. Fix a typo, clarify a section, add an example — no contribution is too small.

## Development Setup

```bash
git clone https://github.com/jonajinga/broadsheet.git
cd broadsheet
npm install
npm start
```

The site builds and serves at `http://localhost:8080` with live reload.

## Code Standards

Broadsheet is deliberately built without frameworks. Please follow these conventions:

- **CSS**: Vanilla CSS with custom properties. No Tailwind, no SCSS, no CSS-in-JS. Use the design tokens in `tokens.css`. BEM naming convention (`.block__element--modifier`).
- **JavaScript**: Vanilla JS. No React, no Vue, no jQuery. Each feature gets its own file, loaded with `defer`. No bundler.
- **HTML**: Nunjucks templates. Semantic HTML. ARIA labels on interactive elements. 44px minimum touch targets.
- **Accessibility**: WCAG 2.2 AA minimum. 4.5:1 contrast for text. Visible focus indicators. Keyboard navigable.
- **Performance**: No unnecessary dependencies. Lazy-load where possible. Total JS should stay under 250 KB.

## Commit Messages

Use clear, descriptive commit messages:
- `Add: new feature description`
- `Fix: bug description`
- `Update: what changed and why`
- `Remove: what was removed and why`

## Pull Request Guidelines

- Keep PRs focused — one feature or fix per PR
- Include a clear description of what changed and why
- Test on both light and dark mode
- Test on mobile (320px minimum)
- Ensure the build passes (`npm run build`)

## Issue Labels

| Label | Description |
|---|---|
| `bug` | Something is broken |
| `enhancement` | Feature request |
| `documentation` | Documentation improvement |
| `good first issue` | Good for newcomers |
| `help wanted` | Looking for contributors |
| `design` | Visual/UI change |
| `accessibility` | Accessibility improvement |
| `performance` | Performance optimisation |

## Code of Conduct

This project follows the [Contributor Covenant](CODE_OF_CONDUCT.md). By participating, you agree to uphold this code.

## Questions?

Open an issue or email [jonajinga@gmail.com](mailto:jonajinga@gmail.com).
