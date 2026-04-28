<div align="center">

# RedMate

**Native macOS desktop client for Xiaohongshu (RED · Little Red Book) — multi-account, auto-publish, scheduled posts, built-in MCP Server.**

[![macOS](https://img.shields.io/badge/macOS-12%2B-black?logo=apple&logoColor=white)](#)
[![Electron](https://img.shields.io/badge/Electron-2B2E3A?logo=electron&logoColor=white)](#)
[![MCP](https://img.shields.io/badge/MCP-Server-7c3aed)](#)
[![License](https://img.shields.io/badge/license-Commercial-d7472e)](#)

[Website](https://redmate.app) · [Download](https://redmate.app/download) · [Docs](https://redmate.app/docs) · [简体中文](README.md)

</div>

---

## What is RedMate

**RedMate** is a native macOS desktop assistant for **Xiaohongshu** (also known as **Little Red Book**, **RED**, **XHS**, or **小红书**) — China's largest lifestyle and shopping social network with 300M+ monthly active users.

It puts everything Xiaohongshu creators do every day — login, publish image notes, publish video notes, schedule content, manage multiple accounts — into one Mac app. And it ships with a built-in **MCP (Model Context Protocol) Server** so you can drive your Xiaohongshu account from **Claude Desktop**, **Cursor**, **Cline**, or any MCP-compatible AI client.

## Why RedMate

- 🍎 **Truly native macOS** — not a web wrapper. Native menubar, tray, notifications, dark mode
- 🔐 **Multi-account, isolated** — every account in its own browser session, no cookie cross-contamination
- ✍️ **Image & video notes** — pick photos, write captions, add hashtags, mention users, set location, crop covers
- ⏰ **Scheduled posts** — queue a week of content, the app keeps the schedule running in the background
- 🤖 **Built-in MCP Server** — let Claude / Cursor / Cline operate your account through the standard MCP protocol
- 🔒 **Local-first, encrypted** — cookies stored via macOS Keychain (`safeStorage`). Your credentials never leave your Mac
- 🎯 **Production-grade automation** — driven by Chrome DevTools Protocol, not brittle DOM scripts

## Features

| Module | Capability |
|---|---|
| **Accounts** | QR-code login · multi-account · Keychain-encrypted cookies · auto-renewal |
| **Publishing** | Image notes · video notes · hashtags / mentions / location · cover crop · drafts |
| **Scheduling** | Publish queue · background daemon · auto-retry · resume after restart |
| **MCP** | HTTP SSE Server · standard MCP protocol · Claude / Cursor / Cline compatible |
| **Sync** | Cross-device drafts · team workspace (Pro) |

## Screenshots

> Screenshots will be added during public beta.

## Install

| Channel | Status |
|---|---|
| DMG via redmate.app (notarized) | Private beta |
| Mac App Store | Coming soon |

👉 **Join the beta at [redmate.app](https://redmate.app).**

## MCP Integration

When RedMate is running, it exposes a local MCP HTTP SSE Server on `127.0.0.1`. Add this to your Claude Desktop config:

```json
{
  "mcpServers": {
    "redmate": {
      "url": "http://127.0.0.1:PORT/sse"
    }
  }
}
```

Then talk to Claude:

> "Check what comments came in on my Xiaohongshu today and pick three worth replying to. Reply from my account."
>
> "Schedule three skincare notes this week — Wed, Fri, Sun at noon."
>
> "Take this set of photos and post them with the hashtag #autumn-outfit."

Tools available today:

- `xhs_list_accounts` — list logged-in accounts
- `xhs_get_active_account` — current active account
- `xhs_set_active_account` — switch account
- `xhs_check_login` — verify login state
- `xhs_publish_note` — publish an image note

More tools (video publishing, scheduling, comments / DMs, analytics) are rolling out.

## System Requirements

- **macOS 12** (Monterey) or later
- **Apple Silicon** and **Intel** both supported
- ~200 MB disk space

## FAQ

**Is this open source?**
No. RedMate is a commercial product. This repository is only for product information and release notes.

**Will my account get banned?**
RedMate closely mimics real human browser behavior and never calls private Xiaohongshu APIs. That said, no third-party tool can fully guarantee platform-policy outcomes — please use responsibly.

**Windows / Linux?**
macOS only for now. Windows is on the roadmap but lower priority; no Linux plans.

**Pricing?**
Free tier plus Pro / Team subscriptions. See the website for details.

## Roadmap

- [x] Multi-account management & auto-login detection
- [x] Image-note publishing
- [x] Built-in MCP Server
- [ ] Video-note publishing
- [ ] Scheduled posts
- [ ] Analytics dashboard (note performance · follower growth)
- [ ] Comments / DM AI assistant
- [ ] Team workspace
- [ ] Mac App Store release

## Keywords

xiaohongshu · xhs · redbook · little red book · RED · 小红书 · xiaohongshu automation · xiaohongshu publishing tool · xiaohongshu desktop client · xiaohongshu mac client · xiaohongshu mcp · MCP server · Model Context Protocol · Claude · Cursor · Cline · AI agent · content creation · social media management · creator tools

## Contact

- Website: [redmate.app](https://redmate.app)
- Email: [support@redmate.app](mailto:support@redmate.app)
- Feedback: open an [Issue](../../issues)

---

<div align="center">

**RedMate · Let AI run your Xiaohongshu.**

Made with 🍎 on macOS

</div>
