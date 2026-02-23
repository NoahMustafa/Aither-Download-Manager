<div align="center">

<!--
  SCREENSHOT NOTE: Replace the line below with your actual app icon/logo.
  Recommended: a 128x128 or 256x256 PNG of the Aither icon.
  Example: <img src="docs/assets/icon.png" width="120" alt="Aither icon" />
-->
<img src="docs/assets/icon.png" width="120" alt="Aither" />

# Aither

**A next-generation download manager built for speed, privacy, and simplicity.**

[![Version](https://img.shields.io/badge/version-0.1.0--beta-a78bfa?style=flat-square)](https://github.com/NoahMustafa/Aither-Download-Manager/releases/tag/v0.1.0)
[![Platform](https://img.shields.io/badge/platform-Windows-0078d4?style=flat-square&logo=windows)](https://github.com/NoahMustafa/Aither-Download-Manager/releases/tag/v0.1.0)
[![Built with Tauri](https://img.shields.io/badge/built%20with-Tauri-24c8db?style=flat-square&logo=tauri)](https://tauri.app)
[![Built with Rust](https://img.shields.io/badge/engine-Rust-f74c00?style=flat-square&logo=rust)](https://www.rust-lang.org)
[![PayPal](https://img.shields.io/badge/Donate-PayPal-0070ba?style=flat-square&logo=paypal&logoColor=white)](https://paypal.me/MahmoudMustafa186)
[![Ko-fi](https://img.shields.io/badge/Support-Ko--fi-ff5e5b?style=flat-square&logo=ko-fi&logoColor=white)](https://ko-fi.com/noah_mustafa_stuff)

[**Download**](https://github.com/NoahMustafa/Aither-Download-Manager/releases/tag/v0.1.0) · [**Report a Bug**](https://github.com/NoahMustafa/Aither-Download-Manager/issues) · [**Request a Feature**](https://github.com/NoahMustafa/Aither-Download-Manager/issues) · [**Buy me a coffee ☕**](https://ko-fi.com/noah_mustafa_stuff)

</div>

---

<!--
  SCREENSHOT NOTE: Replace the image below with a full-width screenshot of the main
  download list — ideally showing 2-3 active downloads with progress bars, speed, and ETA.
  Recommended size: 1280x800 or wider. Save as docs/assets/screenshot-main.png
-->

![Aither main window](docs/assets/screenshot-main.png)

---

## What is Aither?

Aither is a free, freemium download manager that replaces your browser's built-in downloader with something far more capable. It intercepts downloads automatically, splits files into parallel connections for maximum speed, survives crashes without losing progress, and pulls videos and playlists from over 1000 websites, and ability to download torrents with up-to-date daily trackers — all from a clean, modern interface.

---

## Features

### Native Download Engine

- **Multi-connection parallel downloads** — splits files into chunks and downloads simultaneously
- **HTTP, HTTPS, FTP, and FTPS** support out of the box
- **Crash-resistant** — state is saved continuously; resume exactly where you left off after a crash or restart
- **Auto-retry** on network drops with intelligent backoff

### Media Downloads

- **1000+ supported sites** via yt-dlp — YouTube, Vimeo, Twitter/X, Reddit, Instagram, TikTok, Dailymotion, Twitch, and many more
- **Quality selector** — choose resolution, format, and audio tracks before downloading
- **Playlist support** — download entire playlists or channels in one go
- **Cookie-based authentication** — access private, login-protected, and age-restricted content using your browser session

### Browser Extension

- **Automatic download interception** — every download link in your browser is routed through Aither
- **In-page overlay button** — a download button appears directly on top of videos as you browse; no copy-pasting URLs
- **Blacklist** — exclude specific domains so the browser handles them natively

### Torrent

- **Torrent and magnet link support** via aria2c
- Configurable connections and speed limits per download

### General

- **Auto-update** — lightweight background updates without reinstalling
- **System tray** — runs quietly in the background, always available
- **Proxy support** — per-download or global proxy configuration
- **Speed limits** — set global or per-engine download caps
- **16 languages** — Arabic, Chinese, Dutch, English, French, German, Hindi, Indonesian, Italian, Japanese, Korean, Norwegian, Polish, Portuguese, Russian, Spanish, Swedish, Turkish

---

## Screenshots

<details>
<summary>Click to expand screenshots</summary>

<br>

<!--
  SCREENSHOT NOTE: A close-up of a single active download showing the progress bar,
  speed (MB/s), ETA, file name, and the pause/cancel buttons.
  Save as: docs/assets/screenshot-download-progress.png
-->

### Active Download

![Active download progress](docs/assets/screenshot-download-progress.png)

---

<!--
  SCREENSHOT NOTE: The yt-dlp analyzer/quality selector dialog that opens when a media
  URL is detected. Should show the format list (1080p, 720p, audio-only, etc.)
  and the "Use Site Cookies" checkbox.
  Save as: docs/assets/screenshot-media-analyzer.png
-->

### Media Quality Selector

![Media quality selector](docs/assets/screenshot-media-analyzer.png)

---

<!--
  SCREENSHOT NOTE: A browser page (e.g. a video site) with the Aither overlay download
  button visible on top of a video thumbnail. Shows the extension in action.
  Save as: docs/assets/screenshot-overlay.png
-->

### In-Page Overlay Button

![In-page overlay download button](docs/assets/screenshot-overlay.png)

---

<!--
  SCREENSHOT NOTE: The browser extension popup showing the Features toggles
  (Intercept Downloads, Detect Media) and the Blacklist section.
  Save as: docs/assets/screenshot-extension-popup.png
-->

### Browser Extension

![Browser extension popup](docs/assets/screenshot-extension-popup.png)

---

<!--
  SCREENSHOT NOTE: The Settings page inside the Aither app — showing speed limits,
  connection count, language selector, and proxy settings.
  Save as: docs/assets/screenshot-settings.png
-->

### Settings

![Settings](docs/assets/screenshot-settings.png)

</details>

---

## Installation

### Option 1 — MSI Installer (Recommended)

1. Download **`Aither_0.1.0_x64.msi`** from the [latest release](https://github.com/NoahMustafa/Aither-Download-Manager/releases/tag/v0.1.0)
2. Run the installer and follow the prompts
3. Aither launches automatically and appears in the system tray

### Option 2 — Portable

> Coming in a future release.

### System Requirements

|             | Minimum                         |
| ----------- | ------------------------------- |
| **OS**      | Windows 10 64-bit (build 1903+) |
| **RAM**     | 100 MB                          |
| **Disk**    | 200 MB                          |
| **Network** | Any                             |

---

## Browser Extension Setup

The browser extension enables automatic download interception and the in-page overlay button.

1. Install Aither — the extension files are bundled with the app and extracted automatically on first run
2. Open Chrome and go to `chrome://extensions`
3. Enable **Developer mode** (top-right toggle)
4. Click **Load unpacked** and select the folder:
   ```
   %LOCALAPPDATA%\Aither\extension\chrome
   ```
5. The Aither icon appears in your toolbar — you're done

> **Note:** The extension connects to the Aither app automatically. No manual configuration is required.

---

## How It Works

```
Browser / URL
     │
     ▼
Browser Extension ──intercepts──► Aither App
                                       │
                          ┌────────────┼────────────┐
                          ▼            ▼             ▼
                    Native Engine   yt-dlp        aria2c
                  (HTTP/FTP files) (media/video) (torrents)
                          │            │             │
                          └────────────┴─────────────┘
                                       │
                                  Downloaded File
```

- **Regular files** (`.zip`, `.exe`, `.pdf`, etc.) → Native engine with parallel chunks
- **Media URLs** (YouTube, Instagram, etc.) → yt-dlp with quality selection
- **Torrents / Magnets** → aria2c

---

## Built With

| Layer             | Technology                                                                |
| ----------------- | ------------------------------------------------------------------------- |
| Desktop framework | [Tauri](https://tauri.app)                                                |
| Backend / Engine  | [Rust](https://www.rust-lang.org) + [Tokio](https://tokio.rs)             |
| Frontend          | [React](https://react.dev) + [TypeScript](https://www.typescriptlang.org) |
| Database          | SQLite via [sqlx](https://github.com/launchbadge/sqlx)                    |
| Media downloads   | [yt-dlp](https://github.com/yt-dlp/yt-dlp)                                |
| Torrents          | [aria2c](https://aria2.github.io)                                         |
| Styling           | [Tailwind CSS](https://tailwindcss.com)                                   |

---

## Roadmap

- [ ] macOS and Linux support
- [ ] Firefox extension
- [ ] Scheduler (download at specific times)
- [ ] Browser extension for Edge and Firefox
- [ ] Batch URL import
- [ ] Post-download actions (extract, run, etc.)

---

## Privacy & Your Data

**Aither does not collect, upload, or share any of your data.** Everything stays on your machine.

### Cookies

When you enable "Use Site Cookies" for a media download, your browser sends the cookies for that site to Aither — the same way your browser would send them to the website itself. Aither uses them **only** to authenticate the download request (so yt-dlp can access private or login-protected content). They are never sent anywhere else.

Here is exactly what happens to your cookies, step by step:

1. **Received** from the browser extension over a local connection — no internet involved
2. **Encrypted immediately** using AES-256-GCM with a key derived from your machine's hardware ID. This means the encrypted file is tied to your specific machine and cannot be decrypted on any other computer
3. **Written to a temporary file** on your local disk (under `%APPDATA%\Aither\cookies\`) only for the duration of the download
4. **Passed to yt-dlp** via the standard `--cookies` flag on your local machine
5. **Deleted** after the download completes

### Logs

Application logs are encrypted in production builds using a hybrid RSA-2048 + AES-256-GCM scheme. Before encryption, all sensitive values (cookies, tokens, passwords, session IDs) are **automatically redacted** and replaced with `[REDACTED]` — so even the encrypted log file never contains your actual cookie values.

### What Aither Does Contact the Internet For

The **only** external contact Aither makes is to **GitHub**, and only for:

- Checking for application updates (`github.com/NoahMustafa/Aither-Download-Manager`)
- Downloading updated versions of bundled tools (yt-dlp, aria2c, ffmpeg) from their official GitHub releases

No user data, download history, machine information, or analytics are included in any of these requests.

### Summary

| Data              | Stored                             | Encrypted                    | Uploaded |
| ----------------- | ---------------------------------- | ---------------------------- | -------- |
| Your cookies      | Temporarily, locally               | Yes — AES-256-GCM            | Never    |
| Your downloads    | Locally (your chosen folder)       | No                           | Never    |
| Application logs  | Locally (`%APPDATA%\Aither\logs\`) | Yes — RSA-2048 + AES-256-GCM | Never    |
| Usage / analytics | Not collected                      | —                            | Never    |

---

## Support the Project

Aither is **completely free** — no ads, no subscriptions, no paywalls, no profit motive. Every feature is available to every user at no cost.

If Aither saves you time and you'd like to say thanks, a small donation helps cover the cost of keeping the project alive: tooling, and continued development. It is entirely optional and never expected.

<div align="center">

[![PayPal](https://img.shields.io/badge/Donate-PayPal-0070ba?style=for-the-badge&logo=paypal&logoColor=white)](https://paypal.me/MahmoudMustafa186)
[![Ko-fi](https://img.shields.io/badge/Support-Ko--fi-ff5e5b?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/noah_mustafa_stuff)

</div>

> Donating does not unlock any features — everything is already free. It simply helps keep the lights on.

---

## Acknowledgements

Aither would not be possible without these incredible open source projects:

- **[yt-dlp](https://github.com/yt-dlp/yt-dlp)** — the powerful media extraction engine behind Aither's video and audio downloads. A massive thanks to the yt-dlp team and all its contributors for maintaining support for 1000+ sites and keeping it free for everyone.

- **[aria2](https://github.com/aria2/aria2)** — the lightweight, high-performance download utility that powers Aither's torrent and magnet link support. Thank you to the aria2 team for building such a reliable and capable tool.

- **[FFmpeg](https://ffmpeg.org)** — the industry-standard multimedia framework used for merging and converting media streams. Thank you to the FFmpeg project and its contributors.

These projects are distributed under their respective open source licenses. Aither bundles their binaries solely for user convenience — all credit belongs to their respective authors and communities.

---

## Contributing

Contributions, bug reports, and feature requests are welcome. Please open an issue before submitting a pull request so we can discuss the approach.

---

## License

Aither is **free to use** but **not open source**. The source code is proprietary and may not be copied, modified, redistributed, or used to build derivative products without explicit written permission from the Aither Team.

**What you can do:**
- Download and use Aither for personal or commercial purposes at no cost
- Report bugs and suggest features

**What you cannot do:**
- Redistribute, repackage, or resell Aither or its components
- Decompile, reverse engineer, or modify the application
- Use the source code or assets in other projects

### Content & Copyright Notice

Aither is a download tool. It does not host, distribute, or provide access to any content. It simply helps you download files and media that you access through your own browser and accounts.

**Aither does not encourage or condone:**
- Downloading copyrighted content without the rights holder's permission
- Circumventing DRM or access controls
- Violating the terms of service of any platform

You are solely responsible for ensuring that your use of Aither complies with applicable laws and the terms of the platforms you interact with. The developers of Aither assume no liability for how the software is used.

### Disclaimer

Aither is provided **as-is**, without any warranty of any kind — express or implied. By using Aither, you agree to the following:

- **We are not responsible for anything you download.** What you choose to download using Aither is entirely your own decision and your own responsibility.
- **No security guarantees.** While we have implemented reasonable security measures (encrypted cookies, encrypted logs, no telemetry, local-only data), Aither is not a certified or audited security product. No software is 100% secure. Vulnerabilities may exist.
- **Security issues will be addressed promptly.** If a security issue is discovered, we will make every reasonable effort to investigate and release a fix as quickly as possible. However, we cannot guarantee a specific response time or that all issues will be resolved.
- **Keep the app updated.** Security fixes and patches are delivered through app updates. We strongly recommend keeping Aither up to date at all times. Outdated versions may contain known vulnerabilities that have already been patched in newer releases.
- **Use at your own risk.** The Aither Team provides this software in good faith and with genuine effort toward quality and security, but we make no guarantees about fitness for any particular purpose, uninterrupted operation, or freedom from bugs or security flaws.

The Aither Team shall not be held liable for any damages, data loss, legal consequences, or other harm arising from the use or misuse of this software.

---

<div align="center">
  <sub>Built with care by the Aither Team</sub>
</div>
