<div align="center">

# RedMate

**Native macOS desktop client for Xiaohongshu (RED · Little Red Book) — multi-account, auto-publish, scheduled posts, built-in MCP Server.**

[![macOS](https://img.shields.io/badge/macOS-12%2B-black?logo=apple&logoColor=white)](#)
[![Electron](https://img.shields.io/badge/Electron-2B2E3A?logo=electron&logoColor=white)](#)
[![MCP](https://img.shields.io/badge/MCP-Server-7c3aed)](#)
[![License](https://img.shields.io/badge/license-Proprietary-d7472e)](LICENSE)

[Website](https://redmate.app) · [简体中文](README.md)

</div>

---

## What is RedMate

**RedMate** is a native macOS desktop assistant for **Xiaohongshu** (also known as **Little Red Book**, **RED**, **XHS**, or **小红书**) — China's largest lifestyle and shopping social network with 300M+ monthly active users.

It puts everything Xiaohongshu creators do every day — login, publish image notes, schedule content, manage multiple accounts — into one Mac app. And it ships with a built-in **MCP (Model Context Protocol) Server** so you can drive your Xiaohongshu account from **Claude Desktop**, **Cursor**, **Cline**, or any MCP-compatible AI client.

## Why RedMate

- 🍎 **Truly native macOS** — not a web wrapper. Native menubar, tray, notifications, dark mode
- 🔐 **Multi-account, isolated** — every account in its own browser session, no cookie cross-contamination
- ✍️ **Image-note publishing** — pick photos, write captions, add hashtags, mention users, set location, crop covers
- ⏰ **Scheduled posts** — queue a week of content, the app keeps the schedule running in the background
- 🤖 **Built-in MCP Server** — let Claude / Cursor / Cline operate your account through the standard MCP protocol
- 🔒 **Local-first, encrypted** — cookies stored via macOS Keychain (`safeStorage`). Your credentials never leave your Mac
- 🎯 **Production-grade automation** — driven by Chrome DevTools Protocol, not brittle DOM scripts

## Features

| Module | Capability | Status |
|---|---|---|
| **Accounts** | QR-code login · multi-account · Keychain-encrypted cookies · auto-renewal | ✅ Shipped |
| **Image notes** | Image notes · hashtags / mentions / location · cover crop · drafts | ✅ Shipped |
| **Scheduling** | Publish queue · background daemon · auto-retry · resume after restart | ✅ Shipped |
| **MCP** | HTTP SSE Server · standard MCP protocol · Claude / Cursor / Cline compatible | ✅ Shipped |
| **Video notes** | Video notes · multi-segment covers · captions | 🚧 In progress |
| **Comments / DM** | AI auto-reply · keyword routing · inbox | 🚧 Planned |
| **Analytics** | Note performance · follower growth · engagement trends | 🚧 Planned |
| **Sync & team** | Cross-device drafts · team workspace | 🚧 Pro · Planned |

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

> "Create a draft for this skincare note and schedule it for Wednesday at noon. Use hashtags #autumn-skincare and #daily."
>
> "Take this set of photos and post them right now with the hashtag #autumn-outfit."
>
> "Show me which accounts I have logged in, and switch the active one to 'daily-thoughts'."

### Available MCP Tools (17)

**Accounts**
- `xhs_list_accounts` — list logged-in accounts
- `xhs_get_active_account` — get the current active account
- `xhs_set_active_account` — switch the active account
- `xhs_check_login` — verify login state
- `xhs_open_login_window` — open the QR-code login window
- `xhs_remove_account` — remove an account

**Drafts**
- `xhs_draft_create` — create a draft
- `xhs_draft_get` — get draft details
- `xhs_draft_list` — list drafts
- `xhs_draft_update` — update a draft
- `xhs_draft_delete` — delete a draft
- `xhs_draft_publish_now` — publish a draft immediately
- `xhs_draft_schedule` — schedule a draft for later

**Publishing & Tasks**
- `xhs_publish_note` — publish an image note directly
- `xhs_publication_tasks_list` — list publication tasks
- `xhs_publication_tasks_get` — get task details
- `xhs_publication_tasks_cancel` — cancel a scheduled publication

More tools (video publishing, comments / DMs, analytics) are rolling out.

## System Requirements

- **macOS 12** (Monterey) or later
- **Apple Silicon** and **Intel** both supported
- ~300 MB disk space

## FAQ

**Is this open source?**
No. RedMate is a commercial product. This repository is only for product information and release notes. See [LICENSE](LICENSE).

**Will my account get banned?**
RedMate closely mimics real human browser behavior and never calls private Xiaohongshu APIs. That said, no third-party tool can fully guarantee platform-policy outcomes — please use responsibly.

**Windows / Linux?**
macOS only for now. Windows is on the roadmap but lower priority; no Linux plans.

**Pricing?**
Free tier plus Pro / Team subscriptions. See the website for details.

**vs. open-source CLI tools?**
CLIs are great for developers. RedMate is built for every creator — full GUI, scheduling, multi-account, AI co-piloting — things a CLI cannot give you.

## Roadmap

- [x] Multi-account management & auto-login detection
- [x] Image-note publishing
- [x] Built-in MCP Server
- [x] Scheduled posts (draft scheduling + task management)
- [ ] Video-note publishing
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
