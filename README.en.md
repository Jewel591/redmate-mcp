<div align="center">

# RedMate · 小薯兔 🍠

**A Mac desktop assistant built for Xiaohongshu (RED · Little Red Book) creators — multi-account, batch publish, scheduled posts.**

> Chinese name: **小薯兔** (xiǎo shǔ tù — "little sweet-potato bunny")

[![macOS](https://img.shields.io/badge/macOS-12%2B-black?logo=apple&logoColor=white)](#)
[![Beta](https://img.shields.io/badge/Beta-Private%20Beta-f59e0b)](#)
[![License](https://img.shields.io/badge/license-Proprietary-d7472e)](LICENSE)

[Website](https://redmate.app) · [简体中文](README.md)

</div>

---

## What is RedMate

**RedMate · 小薯兔** is a Mac desktop app that lets you manage multiple **Xiaohongshu** (also known as **Little Red Book**, **RED**, **XHS**, or **小红书**) accounts on your own Mac, batch-publish image notes, and schedule posts to go out on time.

It also works with AI assistants like ChatGPT and Claude — say "post this set of photos with the hashtag #autumn-outfit on Wednesday at noon" and the AI does the rest.

Xiaohongshu is China's largest lifestyle and shopping social network with 300M+ monthly active users. Creators who post there every day deserve a tool that scales their work, not one that gets in the way.

## Why RedMate

- 🍎 **Built for Mac** — menubar, tray, system notifications, dark-mode follow; fits the way you already use macOS
- 🔐 **Multi-account, isolated** — each account in its own session, no cookie cross-contamination, no constant re-scanning QR codes
- ✍️ **Image-note publishing** — pick photos, write captions, add hashtags, mention users, set location, crop covers — all in-app
- ⏰ **Scheduled posts** — queue a week of content; if your Mac sleeps or restarts, the schedule resumes where it left off
- 🤖 **AI assistant mode** — let Claude / ChatGPT pick topics, draft captions, and publish for you end-to-end
- 🔐 **Account credentials stay local** — login data is encrypted via the macOS Keychain; **nothing is uploaded to the cloud**
- 🛡️ **Reliable** — built to last; we keep up with Xiaohongshu's UI changes so you don't have to

## Privacy & Security

Trusting a third-party tool with your accounts is a high-anxiety move, so we put the rules up front:

- **Local-first** — your notes, drafts, and login sessions live on your Mac
- **No content collection** — we never read or upload your post content, images, or DMs
- **Encrypted at rest** — login data is encrypted via the macOS Keychain
- **Real-browser operation** — RedMate logs in and posts through a real browser on your Mac, **no different from how you'd do it by hand**, and never calls undocumented Xiaohongshu APIs

> No third-party tool can fully guarantee platform-policy outcomes — please use responsibly.

## Features

| Module | Capability | Status |
|---|---|---|
| **Accounts** | QR-code login · multi-account · Keychain-encrypted · auto-renewal | ✅ Shipped |
| **Image notes** | Image notes · hashtags / mentions / location · cover crop · drafts | ✅ Shipped |
| **Scheduling** | Publish queue · background daemon · auto-retry · resume after restart | ✅ Shipped |
| **AI integration** | Compatible with Claude / ChatGPT and major AI assistants | ✅ Shipped |
| **Video notes** | Video notes · multi-segment covers · captions | 🚧 In progress |
| **Comments / DM** | AI auto-reply · keyword routing · inbox | 🚧 Planned |
| **Analytics** | Note performance · follower growth · engagement trends | 🚧 Planned |
| **Sync & team** | Cross-device drafts · team workspace | 🚧 Pro · Planned |

## Screenshots

> Demo videos and screenshots will be added before public beta.

## Who It's For

- 📒 **Independent creators** — get out of phones and browsers, spend more time on ideas and content
- 🏢 **MCN agencies / studios** — manage many creator accounts at once, schedule and dispatch in batches
- 💼 **Brand operators / managed accounts** — schedule posts for clients, never miss a publish window
- 🤖 **AI-first creators** — already using ChatGPT / Claude to draft? Let the AI take it all the way to publish

## Install & Try

| Channel | Status |
|---|---|
| DMG via redmate.app (notarized) | Private beta |
| Mac App Store | Coming soon |

👉 **Join the beta at [redmate.app](https://redmate.app).**

> Free during the private beta. The release version will offer a Free tier plus Pro / Team subscriptions.

## Working with AI Assistants

If you already use Claude, ChatGPT, or similar AI clients, RedMate lets the AI drive your Xiaohongshu account directly.

Talk to your AI like this:

> "Create a draft for this skincare note and schedule it for Wednesday at noon. Use hashtags #autumn-skincare and #daily."
>
> "Take this set of photos and post them right now with the hashtag #autumn-outfit."
>
> "Show me which accounts I have logged in, and switch the active one to 'daily-thoughts'."

The AI calls RedMate's publish, schedule, and account-management capabilities behind the scenes — you don't open a browser or edit config files.

> For developers: RedMate connects to AI clients via the standard MCP (Model Context Protocol). See the [developer docs](https://redmate.app/docs/mcp) (in progress) for setup details.

## System Requirements

- **macOS 12** (Monterey) or later
- **Apple Silicon** (M-series) and **Intel** Macs both supported
- ~300 MB disk space

## FAQ

**Will my account get banned?**
RedMate logs in and posts through a real browser on your own Mac — no different from doing it by hand — and never calls undocumented Xiaohongshu APIs. That said, platform policy itself carries inherent uncertainty, so please use responsibly.

**Windows / Linux?**
macOS only for now. Windows is on the roadmap but lower priority; no Linux plans.

**Pricing?**
Free during the private beta. The release version will offer a Free tier plus Pro / Team subscriptions, with pricing announced before public beta.

**Is my account data uploaded?**
No. Notes, drafts, and login sessions stay on your Mac. Login data is encrypted via the macOS Keychain.

## Roadmap

- [x] Multi-account management & auto-login detection
- [x] Image-note publishing
- [x] Scheduled posts (draft scheduling + task management)
- [x] AI assistant integration
- [ ] Video-note publishing (2026 Q3)
- [ ] Analytics dashboard: note performance · follower growth (2026 Q3)
- [ ] Comments / DM AI assistant (2026 Q4)
- [ ] Team workspace (Pro)
- [ ] Mac App Store release

## Keywords

xiaohongshu · xhs · redbook · little red book · RED · 小红书 · xiaohongshu mac client · xiaohongshu desktop assistant · xiaohongshu scheduling tool · xiaohongshu multi-account · xiaohongshu batch publish · MCN tool · creator tools · social media management · content creation

## Contact

- Website: [redmate.app](https://redmate.app)
- Email: [ivensliao@qq.com](mailto:ivensliao@qq.com)
- Feedback: open an [Issue](../../issues)

---

<div align="center">

**RedMate · 小薯兔 🍠 · A Mac desktop assistant for Xiaohongshu creators**

Made for Mac creators

</div>
