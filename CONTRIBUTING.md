# Contributing to DIABOLIC FRANCE

Thank you for your interest in contributing to **DIABOLIC FRANCE** 🔪🇫🇷.
This project is defensive and educational OSINT: we prioritize **quality, legality, and respect**.

## 📜 Code of Conduct

By participating, you agree to abide by the [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
Be respectful, constructive, and professional.

## 🐛 Reporting a bug

Before opening an issue:

1. Search the [existing issues](https://github.com/Condor2026/diabolic_france_v3/issues) to see if it's already reported.
2. Reproduce the failure with the latest version (`main`).
3. Run the diagnostic:
   ```bash
   python diabolic_france_v3.py --debug-fuente "Source name"
   ```

When opening the issue, include:

- **DIABOLIC FRANCE version** (`v3.0`, commit or tag)
- **OS and Python version**
- **Steps to reproduce**
- **Expected vs. actual behavior**
- **Relevant logs** (no personal data)
- Screenshots if applicable

## 💡 Proposing an improvement

Open an issue with the `enhancement` label explaining:

- The problem it solves
- The proposed solution
- Alternatives considered
- Impact on sources / classification / performance

## 🔧 Pull Requests

1. Fork the repository.
2. Create a descriptive branch:
   ```bash
   git checkout -b fix/alarm-cluster-detect
   ```
3. Follow the existing code style (Python 3.8+, no new dependencies unless justified).
4. Add/update tests if you touch classification, fusion, or geolocation.
5. Update `CHANGELOG.md` and `README.md` if behavior changes.
6. Verify it works:
   ```bash
   python diabolic_france_v3.py --scan fd --pages 1
   python diabolic_france_v3.py --web --port 5016
   ```
7. Open the PR using the template. A maintainer will review it.

### Rules for PRs

- **One PR = one logical change.** Don't mix refactor + feature + fix.
- **Don't add heavy dependencies** without prior discussion.
- **Don't include personal data** or screenshots with sensitive information.
- **Don't break compatibility** with `diabolic_france.json` (v1/v2/v3).
- **Respect robots.txt and rate limits** of the sources.

## 🧩 Adding new sources

Edit the `_FUENTES_RAW`, `_FUENTES_CYBER_RAW`, or `_FUENTES_GOV_RAW` lists in `diabolic_france_v3.py`.
Requirements for a new source:

- **Public** content accessible without authentication.
- Stable HTML structure or RSS feed.
- French geographic coverage (metropolitan or overseas).
- No hard paywall that blocks scraping.

## 🌍 Translations

Supported languages are FR · ES · EN · IT · DE.
If you add new strings, update **all** translation keys.

## ⚖️ Legal and ethical

- Only **public data** is accessed.
- No security-evasion techniques are implemented.
- Contributions that facilitate surveillance of individuals are not accepted.
- Read [DISCLAIMER.md](DISCLAIMER.md) and [LEGAL_ETHICAL_NOTICE.md](LEGAL_ETHICAL_NOTICE.md).

## 📬 Contact

- Issues: [GitHub Issues](https://github.com/Condor2026/diabolic_france_v3/issues)
- Email: SpectrumSecIt@proton.me

Thank you for helping make DIABOLIC FRANCE better. 🛡️
