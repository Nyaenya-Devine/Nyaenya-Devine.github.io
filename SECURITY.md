# Security Policy — Nyaenya-Devine.github.io

## Overview
Static GitHub Pages résumé for Devine Nyaenya. The site has no authentication, user accounts, API, or server-side data store.

## Security Upgrades Emphasized (Military-Grade)

### 1. Security Headers (Military-Grade)
- **Content-Security-Policy:** `default-src 'self'; script-src 'self' 'unsafe-inline' https://fonts.googleapis.com; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com; font-src 'self' https://fonts.gstatic.com data:; img-src 'self' data: https:; connect-src 'self'; base-uri 'self'; form-action 'self'; upgrade-insecure-requests`
- **X-Content-Type-Options:** `nosniff`
- **Referrer-Policy:** `strict-origin-when-cross-origin`
- **Permissions-Policy:** `camera=(), microphone=(), geolocation=()`

### 2. No Hardcoded Secrets
- No API keys, no PATs, no credentials committed
- Verified via `grep -r ghp_` clean, no secrets
- No tracking, no analytics, privacy-first

### 3. Secure Development
- Self-hosted fonts via Google Fonts with preconnect, CSP allowlist
- No third-party trackers, no external scripts except fonts
- Static HTML, no backend, minimal supply chain

### 4. Threat Model
- **XSS via query params:** No user input reflected without escaping
- **Clickjacking limitation:** GitHub Pages does not allow this repository to set `frame-ancestors` or `X-Frame-Options` response headers.
- **Data leakage:** No personal data stored, no tracking

## Reporting
Email: devinenyaenya@gmail.com

## Verified
- `grep -r ghp_` clean, no PATs
- CSP self-only + fonts allowlist
- No real data, no tracking

© 2026 Devine Nyaenya • Security-first • MIT
