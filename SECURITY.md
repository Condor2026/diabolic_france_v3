# Security Policy — DIABOLIC FRANCE

## Supported versions

| Version | Supported |
|---------|-----------|
| 3.0.x   | ✅ Yes    |
| 2.x     | ⚠️ Critical fixes only |
| 1.x     | ❌ No     |

## Reporting a vulnerability

**Do not open a public issue** for security vulnerabilities.

Send an email to **SpectrumSecIt@proton.me** with the subject:

```
[SECURITY] DIABOLIC FRANCE — <brief description>
```

Include:

- Description of the problem
- Steps to reproduce
- Estimated impact (CVSS if possible)
- Affected version
- Proof of concept (without real third-party data)
- Your name/handle for credits (optional)

### Response times

| Stage | Target time |
|-------|-------------|
| Acknowledgement | 72 h |
| Initial assessment | 7 days |
| Fix / mitigation | 30 days (depending on severity) |
| Coordinated disclosure | 90 days |

## Scope

**In scope:**
- The Flask web server (`--web`)
- `/api/*` and `/stream` (SSE) endpoints
- Exports (JSON/CSV/HTML/GeoJSON)
- State persistence (`*.json`)
- Scraping and auto-discovery

**Out of scope:**
- Vulnerabilities in third-party sites being scraped
- Attacks requiring physical access to the machine
- Social engineering
- DoS via massive request volume to localhost

## Security measures already implemented

- POST protected with `X-DF: 1` header (anti-CSRF from third parties)
- CSV injection-safe (prefix `'` on cells with `= + - @`)
- `http(s)` links only (blocking `javascript:` / `data:`)
- `X-Content-Type-Options: nosniff`
- `Referrer-Policy: no-referrer`
- No personal data collection
- 90s/source budget (anti-global-blocking)
- DNS cache (anti-infinite-retries)

## Best practices for deployments

- Do not expose the panel to the Internet without a reverse proxy + auth.
- Use `--host 127.0.0.1` (default) in local environments.
- Rotate logs and backups periodically.
- Review `estado_fuentes_crime.json` if you add sources.

Thank you for helping keep DIABOLIC FRANCE secure. 🛡️
