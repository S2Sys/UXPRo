# UXPRo: Universal UI/UX Design System

[![Version](https://img.shields.io/badge/version-2.2.0-blue)](./VERSION.json)
[![Compatibility](https://img.shields.io/badge/compatible%20with-Claude%20Code%2C%20Cursor%2C%20Windsurf%2C%20Cline-green)](./UPDATE_GUIDE.md)
[![WCAG 2.1 AA](https://img.shields.io/badge/WCAG-2.1%20AA-green)](./UIUX-MASTER-PROMPT-SYSTEM.md#120-contrast--accessibility-wcag-21-aa-minimum)
[![License](https://img.shields.io/badge/license-MIT-blue)](./LICENSE)

A comprehensive, production-ready UI/UX design system for AI-powered coding assistants. Works with Claude Code, Cursor, Windsurf, Cline, Continue.dev, and any LLM-based code generator.

## 📋 Overview

UXPRo provides **26 detailed sections** of design rules, patterns, and guidelines covering everything from core design laws to advanced data visualization and system maintenance.

### Key Features

✅ **26 Comprehensive Sections**
- 1-14: Foundational design principles and components
- 15: Pre-generation checklist
- 16-25: Advanced patterns and platform-specific guidelines
- 26: Version tracking and update procedures

✅ **WCAG 2.1 AA Compliant**
- 4.5:1 minimum contrast for normal text
- 44×44px minimum touch targets
- Semantic HTML with ARIA labels
- Full keyboard navigation support
- Dark mode support with semantic color tokens

✅ **Production-Ready**
- Mobile-first responsive design (320px - 1536px+)
- 8-point spacing grid system
- 1.25 modular scale typography
- 60-30-10 color distribution rule
- GPU-accelerated animations (transform/opacity only)

✅ **Version Tracked**
- Semantic versioning (MAJOR.MINOR.PATCH)
- `VERSION.json` for automated checking
- Comprehensive update guide
- Breaking changes documentation
- Deprecation windows

## 🚀 Quick Start (2 Minutes)

### For Cursor / Windsurf / Cline
1. Copy `.cursorrules` file to your project root
2. Paste content from `UIUX-SYSTEM-PROMPT.md`
3. Start using in prompts - the AI will follow all rules

### For Claude Code
1. Open Settings → Custom Instructions
2. Paste the `UIUX-SYSTEM-PROMPT.md` content
3. Enable and save

### For System Prompt Integration
1. Open your AI tool's settings
2. Find "System Prompt" or "Custom Instructions"
3. Paste entire content from `UIUX-SYSTEM-PROMPT.md`
4. Save and restart the tool

## 📚 Documentation

### Core Files

| File | Purpose |
|------|---------|
| **UIUX-MASTER-PROMPT-SYSTEM.md** | Complete 26-section design system (4000+ lines) |
| **UIUX-SYSTEM-PROMPT.md** | Condensed version for pasting into AI tools |
| **design-tokens.css** | CSS variable implementation of all tokens |
| **VERSION.json** | Version tracking and update metadata |
| **UPDATE_GUIDE.md** | Step-by-step guide for checking and applying updates |

### Usage Guides

- **[UPDATE_GUIDE.md](./UPDATE_GUIDE.md)** - How to check for updates, apply them, and maintain tokens
- **[CHANGELOG.md](./CHANGELOG.md)** - Version history and changes
- **[CONTRIBUTING.md](./CONTRIBUTING.md)** - How to contribute improvements

## 📖 What's Included

### Sections 1-14: Foundational Rules

1. **Core Design Laws** - 60-30-10 color rule, contrast, typography scale, spacing
2. **Responsive Design Rules** - Mobile-first, breakpoints, fluid typography
3. **Visual Hierarchy** - Z-index scale, shadows, border radius
4. **Component Design Rules** - Buttons, forms, cards, states
5. **Motion & Animation** - Durations, easing, GPU-accelerated transforms
6. **Layout Patterns** - Grids, flexbox, centering
7. **Dark Mode & Theming** - Semantic color tokens, auto-detection
8. **Accessibility (A11Y)** - Focus indicators, ARIA labels, keyboard nav
9. **Performance Optimization** - No layout shifts, efficient animations
10. **Typography Rules** - Font choices, weights, line heights, max-width
11. **Icon & Imagery Rules** - Sizing, stroke, aspect ratios
12. **Interaction States** - Hover, active, focus, disabled, loading
13. **Common Component Specs** - Navigation, modals, toasts, cards
14. **Data Visualization** - Chart colors, dashboard grids, tables

### Sections 15-26: Detailed Patterns & Infrastructure

15. **Design System Checklist** - Pre-generation validation list
16. **Micro-interactions & Feedback** - Skeleton loaders, progress, pull-to-refresh
17. **Navigation Patterns** - Breadcrumbs, tabs, sidebars, bottom sheets
18. **Advanced Form Patterns** - Multi-step wizards, inline editing, file upload
19. **Content Patterns** - Image ratios, avatars, badges, timelines
20. **Error & Edge Cases** - 404/500 pages, offline states, timeouts
21. **Accessibility Deep Dive** - Skip links, live regions, focus traps
22. **Performance UI Patterns** - Lazy loading, infinite scroll, debouncing
23. **Platform-Specific** - iOS, Material Design 3, desktop apps, PWA
24. **Iconography Details** - Sizing scale, stroke width, alignment
25. **Advanced Data Visualization** - Color palettes, KPI cards, advanced tables
26. **System Updates & Maintenance** - Versioning, update procedures, token maintenance

## 🔄 Checking for Updates

### Quick Check
```bash
# Get latest version
curl -s https://raw.githubusercontent.com/s2sys/uxpro/main/VERSION.json | jq '.version'
```

### Full Details
Visit [VERSION.json](./VERSION.json) to see:
- Current version and release date
- All sections included
- Breaking changes (if any)
- Compatibility matrix
- Support windows

See [UPDATE_GUIDE.md](./UPDATE_GUIDE.md) for detailed update procedures.

## 📝 Version History

| Version | Date | Highlights |
|---------|------|-----------|
| **2.2.0** | 2026-04-08 | Added Section 26 (System Updates), VERSION.json, UPDATE_GUIDE.md, version tracking |
| 2.1.0 | 2026-04-08 | Expanded with 10 new sections (16-25) covering micro-interactions through data viz |
| 2.0.0 | 2026-03-15 | Complete redesign with 14 foundational sections |
| 1.0.0 | 2026-01-01 | Initial release |

See [CHANGELOG.md](./CHANGELOG.md) for detailed changes in each version.

## 🛠️ Implementation Examples

### CSS Integration
```html
<!-- Import design tokens -->
<link rel="stylesheet" href="design-tokens.css">

<!-- Use tokens in your styles -->
<style>
  .button {
    padding: var(--space-3) var(--space-4);
    background: var(--accent-500);
    color: white;
    border-radius: var(--radius-md);
    font-size: var(--text-base);
    min-height: 44px; /* Touch target */
    transition: background 200ms ease-out; /* Use ease-out by default */
  }

  .button:hover {
    background: var(--accent-600);
  }

  .button:focus {
    outline: 2px solid var(--accent-700);
    outline-offset: 2px;
  }
</style>
```

### Prompt Integration
```markdown
You are an expert UI/UX designer. Follow these design rules:

[Paste content from UIUX-SYSTEM-PROMPT.md here]

When generating UI components:
1. Apply the 60-30-10 color rule
2. Ensure 4.5:1 text contrast
3. Use 8-point spacing grid
4. Include all interaction states
5. Support dark mode with semantic tokens
6. Verify on mobile (320px) and desktop (1280px+)
```

## 🎯 Best Practices

### When Using with AI Tools

1. **Update Regularly** - Check VERSION.json monthly for new patterns
2. **Review Breaking Changes** - Before major updates, read the migration guide
3. **Test Thoroughly** - Verify responsive design on multiple devices
4. **Use Token Variables** - Never hardcode colors or spacing
5. **Follow the Checklist** - Run through pre-generation checklist before finalizing

### For Teams

1. **Save in Version Control** - Commit VERSION.json and tokens to your repo
2. **Create a Branch** - Test major updates on a feature branch first
3. **Document Overrides** - If modifying tokens, document why in a comment
4. **Share Updates** - Notify team when updating the design system
5. **Monitor Changes** - Watch GitHub for new releases

## 🌐 Supported Platforms

| Platform | Version | Status |
|----------|---------|--------|
| Claude Code | 1.0+ | ✅ Supported |
| Cursor | 0.30+ | ✅ Supported |
| Windsurf | 1.0+ | ✅ Supported |
| Cline | 1.0+ | ✅ Supported |
| Continue.dev | 0.8+ | ✅ Supported |
| Copilot | 1.0+ | ✅ Supported |

## 🤝 Contributing

Found a bug? Have a suggestion? Want to improve the design system?

1. Check [GitHub Issues](https://github.com/s2sys/uxpro/issues) for existing reports
2. Create a new issue with details about:
   - What you found/suggest
   - Current version you're using
   - Steps to reproduce (if applicable)
   - Screenshots or code examples

## 📄 License

This design system is provided as-is for use with AI coding assistants. Feel free to modify for your projects.

## 🔗 Resources

- [WCAG 2.1 Guidelines](https://www.w3.org/WAI/WCAG21/quickref/) - Accessibility standards
- [Web AIM Contrast Checker](https://webaim.org/resources/contrastchecker/) - Test color contrast
- [MDN Web Docs](https://developer.mozilla.org/) - CSS and HTML reference
- [Material Design 3](https://m3.material.io/) - Design system reference
- [iOS Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/) - iOS patterns

## 📞 Support

For questions or issues:
- Check [UPDATE_GUIDE.md](./UPDATE_GUIDE.md) FAQ section
- Review [CHANGELOG.md](./CHANGELOG.md) for known issues
- Visit [GitHub Issues](https://github.com/s2sys/uxpro/issues)

---

**Current Version:** 2.2.0 | **Last Updated:** 2026-04-08 | **Status:** Stable