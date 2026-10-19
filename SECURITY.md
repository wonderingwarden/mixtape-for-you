# Security Policy

## Supported version

Security fixes are intended for the latest version on the default branch.

## Reporting a vulnerability

Please do not publish exploitable details in a public issue. If GitHub private vulnerability reporting is enabled for this repository, use **Security → Report a vulnerability**. Otherwise, contact the repository owner privately before disclosing details publicly.

Include the affected file or feature, reproduction steps, potential impact, and any suggested mitigation. Do not include real people's private mixtape content or personal data in reports.

## Security notes

This is a client-side static application. It requests song data from the iTunes Search API and may load remote artwork, audio previews, and Google Fonts. Never add secrets to client-side code; anything shipped to a browser is public.
