# Security Headers Note — Kaola Product Lab Mobile Gate 2 RC2 R6

Date: 2026-06-03
Scope: Vercel front-end security headers only.

This package adds `vercel.json` with HTTP security headers for the Vercel static deployment layer.

Included headers:

- `X-Content-Type-Options: nosniff`
- `X-Frame-Options: DENY`
- `X-XSS-Protection: 1; mode=block`
- `Referrer-Policy: strict-origin-when-cross-origin`
- `Strict-Transport-Security: max-age=31536000; includeSubDomains; preload`

CSP is intentionally not added in this patch to avoid breaking external links or future third-party routing. CSP should be added later only after resource inventory and deployment QA.
