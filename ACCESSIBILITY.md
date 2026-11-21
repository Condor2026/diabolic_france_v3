# Accessibility Statement — DIABOLIC FRANCE

DIABOLIC FRANCE is committed to making its platform usable by as many people as possible, including users with disabilities. This statement describes our accessibility commitment, supported environments, known limitations, and how to report barriers.

## Our commitment

We aim to follow the principles of the **Web Content Accessibility Guidelines (WCAG) 2.1, Level AA** where feasible for the web dashboard, and to provide a usable terminal interface for screen-reader and keyboard-only users.

We recognize that DIABOLIC FRANCE is a data-heavy OSINT tool and that full accessibility is an ongoing effort. We welcome reports and contributions that improve accessibility.

## Supported environments

| Environment | Status |
|-------------|--------|
| Modern browsers (Chrome, Firefox, Edge, Safari — last 2 versions) | ✅ Supported |
| Screen readers (NVDA, JAWS, VoiceOver, Orca) | ⚠️ Partially supported |
| Keyboard-only navigation | ✅ Supported |
| Terminal (TTY) with screen reader | ⚠️ Partially supported |
| High-contrast / forced-colors mode | ⚠️ Partially supported |
| Zoom up to 200% | ✅ Supported |
| Mobile browsers (responsive layout) | ⚠️ Partially supported |

## Accessibility features

- Semantic HTML structure in the web dashboard (headings, landmarks, lists).
- Keyboard navigation for menus, filters, and toolbar buttons.
- Visible focus indicators on interactive elements.
- Text alternatives for icons and status badges where meaningful.
- Adjustable filter sensitivity and language selection (FR · ES · EN · IT · DE).
- No auto-playing audio without explicit user interaction (alarm requires opt-in).
- Color is not the sole means of conveying status in most views (labels and icons accompany colors).

## Known limitations

- **Charts and maps** (Sankey, heatmap, clusters, choropleth, timelapse) rely on visual rendering (Canvas/SVG/Leaflet) and are **not fully accessible** to screen readers. Data is available via the REST API and exports (JSON/CSV/GeoJSON) as an alternative.
- **Real-time SSE stream** and animated tickers may be distracting; users can stop scans and mute alarms, but a dedicated "reduce motion" toggle is not yet implemented.
- **Terminal menu** uses emoji and box-drawing characters that may be read inconsistently by some screen readers.
- **Color contrast** in the dark theme may not meet AA on all elements; improvements are tracked.
- **Alarm sounds** are audio-only; a visual alarm indicator exists but is not equivalent.
- Some third-party map tiles (Carto, Esri, OSM) are outside our control.

## Reporting an accessibility barrier

If you encounter an accessibility barrier, please report it:

- **Email:** SpectrumSecIt@proton.me — subject: `[A11Y] DIABOLIC FRANCE — <brief description>`
- **GitHub:** open an issue using the bug report template and add the `accessibility` label.

Please include:

- The page, view, or feature affected
- Your browser, OS, and assistive technology (if any)
- Steps to reproduce the barrier
- The impact on your ability to use the feature
- Any suggested improvement (optional)

We aim to acknowledge accessibility reports within **7 days** and to address confirmed barriers in a reasonable timeframe, prioritizing those that block core functionality.

## Continuous improvement

Accessibility is part of our review process. Contributions that improve accessibility (semantic markup, ARIA where appropriate, keyboard support, contrast, reduced motion) are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).

## Contact

- Email: SpectrumSecIt@proton.me
- Project: DIABOLIC FRANCE v3

Thank you for helping make DIABOLIC FRANCE more accessible. 🛡️
