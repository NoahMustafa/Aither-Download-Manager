# Security Policy

## Supported Versions

Only the latest release is supported with security fixes. Aither auto-updates
by default — keeping the app up to date is the primary way vulnerabilities
get patched. See [releases](https://github.com/NoahMustafa/Aither-Download-Manager/releases)
for the current version.

## Reporting a Vulnerability

Please **do not** open a public issue for security vulnerabilities.

Report privately instead:

- Open a [GitHub Security Advisory](https://github.com/NoahMustafa/Aither-Download-Manager/security/advisories/new) (preferred), or
- Email the maintainer via the contact on the [Aither website](https://aither-landing-page.pages.dev/)

Include what you found, steps to reproduce, and impact if known. We'll
acknowledge reports and work on a fix as quickly as possible; response time
isn't guaranteed but security issues are treated as top priority.

## What's in scope

- The Aither desktop app and installer/updater
- The bundled browser extension
- Handling of cookies, credentials, or local data (see the Privacy section in
  [README.md](README.md) for how these are currently handled)

## What's out of scope

- Vulnerabilities in bundled third-party tools (yt-dlp, aria2, FFmpeg) — report
  those upstream to the respective projects
- Aither is closed-source; the underlying code cannot be independently
  audited by reporters. Reports based on behavioral testing of the shipped
  binary are welcome.
