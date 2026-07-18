# Security Policy

## Reporting a Vulnerability

**Please do not open a public GitHub issue for security vulnerabilities.**

If you believe you've found a security issue in TrailGuide Canvas AI Tutor — for example, a way to exfiltrate a user's stored API key, bypass the Content Security Policy, or otherwise compromise a user's browser through the extension — report it privately:

**Email:** bryan.buchorn@gmail.com
**Subject line:** `TrailGuide Security Report`

Please include:
- A description of the vulnerability and its potential impact
- Steps to reproduce (proof-of-concept code or a minimal repro is appreciated)
- The extension version and browser you tested against

## What to Expect

- We aim to acknowledge security reports within **5 business days**.
- We'll let you know once a fix is shipped, and are happy to credit you in the release notes if you'd like.
- Please give us a reasonable window to ship a fix before any public disclosure.

## Scope

TrailGuide runs entirely client-side inside your browser — there is no TrailGuide-operated backend server to attack. Relevant attack surface includes:
- The extension's Content Security Policy and permission model (`manifest.json`)
- Local storage of API keys and their encryption (AES-256-GCM, see the [Privacy Policy](index.html#security))
- Input sanitization of Canvas page content before it's processed or displayed
- The extension's message passing between content scripts and the service worker

Vulnerabilities in third-party services TrailGuide connects to (Google Gemini, OpenAI, Anthropic, Google Drive) should be reported directly to those providers.

## Supported Versions

Only the latest published version of the extension receives security fixes.
