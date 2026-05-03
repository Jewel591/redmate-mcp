<div align="center">

# RedMate

**小红书 macOS 桌面助手 · 多账号 · 自动发布 · 定时发布 · 内置 MCP Server**

[![macOS](https://img.shields.io/badge/macOS-12%2B-black?logo=apple&logoColor=white)](#)
[![Electron](https://img.shields.io/badge/Electron-2B2E3A?logo=electron&logoColor=white)](#)
[![MCP](https://img.shields.io/badge/MCP-Server-7c3aed)](#)
[![License](https://img.shields.io/badge/license-Proprietary-d7472e)](LICENSE)

[官网](https://redmate.app) · [English](README.en.md)

</div>

---

## 简介

**RedMate** 是一款专为小红书（xiaohongshu / xhs / RED / Little Red Book）创作者与内容运营团队打造的 **macOS 原生桌面助手**。它把账号登录、图文笔记发布、定时发布、批量管理这些日常重复劳动从浏览器搬进一个本地 App，并内置 **MCP（Model Context Protocol）Server**，让 Claude、Cursor、Cline 这类 AI 客户端可以直接接管你的小红书账号操作。

> 内容运营值得被工具放大，而不是被工具拖垮。

## 为什么选 RedMate

- 🍎 **macOS 原生体验** — 不是网页套壳，全 Apple 设计语言；原生菜单栏、托盘图标、系统通知、深色模式自动跟随
- 🔐 **多账号并行不串号** — 每个小红书账号独立浏览器会话，cookie 完全隔离，不再频繁切号
- ✍️ **图文笔记发布** — 选图、写文案、加话题、@ 用户、定位、改封面，全部在 App 内完成
- ⏰ **定时发布** — 排好一周内容，App 在后台到点自动发；关机重开任务自动续跑，不丢稿
- 🤖 **MCP Server 内置** — Claude Desktop / Cursor / Cline 通过 MCP 协议直连，**让 AI 帮你选题、写稿、配图、发布全自动**
- 🔒 **本地优先 · 数据加密** — Cookie 走 macOS Keychain（safeStorage）加密落盘，账号资产不离开你的 Mac
- 🎯 **商业级稳定** — 底层用 Chromium DevTools Protocol，行为接近真人浏览器，不靠脆弱的页面注入脚本

## 核心功能

| 模块 | 能力 | 状态 |
|---|---|---|
| **账号管理** | 扫码登录 · 多账号并行 · Cookie Keychain 加密 · 自动续期 | ✅ 已上线 |
| **图文发布** | 图文笔记 · 话题 / @ / 定位 · 封面剪裁 · 草稿箱 | ✅ 已上线 |
| **定时发布** | 发布队列 · 后台保活 · 失败自动重试 · 关机续跑 | ✅ 已上线 |
| **MCP 接入** | HTTP SSE Server · 标准 MCP 协议 · 兼容 Claude / Cursor / Cline | ✅ 已上线 |
| **视频笔记发布** | 视频笔记 · 多片段封面 · 字幕 | 🚧 开发中 |
| **评论 / 私信助手** | AI 自动回复 · 关键词分流 · 收件箱 | 🚧 规划中 |
| **数据看板** | 笔记表现 · 粉丝增长 · 互动趋势 | 🚧 规划中 |
| **同步与协作** | 跨设备草稿同步 · 团队空间 | 🚧 Pro 规划中 |

## 截图

> 内测期间界面仍在打磨，截图将在公测前陆续补齐。

## 安装

| 渠道 | 状态 |
|---|---|
| 官网 dmg 直分发（Apple 公证） | 内测中 |
| Mac App Store | 准备中 |

👉 **加入内测请访问 [redmate.app](https://redmate.app)**

## MCP 集成

RedMate 启动后会在本地 `127.0.0.1` 监听一个 MCP HTTP SSE Server。在 Claude Desktop 配置文件里加上：

```json
{
  "mcpServers": {
    "redmate": {
      "url": "http://127.0.0.1:PORT/sse"
    }
  }
}
```

之后你就可以直接对 Claude 说：

> "把这篇护肤笔记的草稿建好，周三中午 12 点定时发出去，话题用 #秋冬护肤 #日杂风。"
>
> "我刚拍的这组图配段文案直接发出去，话题用 #秋冬穿搭 #日杂风。"
>
> "看下我有几个账号在线，把活跃账号切到『日常碎碎念』那个。"

### 当前可用的 MCP 工具（17 个）

**账号管理**
- `xhs_list_accounts` — 列出已登录账号
- `xhs_get_active_account` — 获取当前活跃账号
- `xhs_set_active_account` — 切换活跃账号
- `xhs_check_login` — 检查登录态
- `xhs_open_login_window` — 打开扫码登录窗口
- `xhs_remove_account` — 移除账号

**草稿管理**
- `xhs_draft_create` — 创建草稿
- `xhs_draft_get` — 获取草稿详情
- `xhs_draft_list` — 草稿列表
- `xhs_draft_update` — 更新草稿
- `xhs_draft_delete` — 删除草稿
- `xhs_draft_publish_now` — 立即发布草稿
- `xhs_draft_schedule` — 定时发布草稿

**发布与任务**
- `xhs_publish_note` — 直接发布图文笔记
- `xhs_publication_tasks_list` — 发布任务列表
- `xhs_publication_tasks_get` — 获取任务详情
- `xhs_publication_tasks_cancel` — 取消发布任务

更多工具（视频发布、评论 / 私信管理、数据看板）正在陆续上线。

## 系统要求

- **macOS 12** (Monterey) 或更高版本
- **Apple Silicon** 与 **Intel** 双架构
- 约 300 MB 安装空间

## 常见问题

**Q：这是开源项目吗？**
A：不是。RedMate 是商业产品，本仓库只用于产品介绍与发布说明，源码不开放。详见 [LICENSE](LICENSE)。

**Q：会被小红书封号吗？**
A：RedMate 高度还原真人浏览器操作，不调用任何小红书未公开接口。但任何第三方工具都无法 100% 担保平台政策风险，请合理使用。

**Q：支持 Windows / Linux 吗？**
A：当前只做 macOS。Windows 在路线图上但优先级靠后；Linux 暂无计划。

**Q：收费吗？**
A：基础版免费，Pro / Team 订阅制。详见官网。

**Q：和开源 CLI 工具相比有什么优势？**
A：CLI 工具适合开发者；RedMate 面向所有内容创作者，提供完整 GUI、定时调度、多账号管理、AI 协作等命令行不具备的能力。

## 路线图

- [x] 多账号管理 · 自动登录态识别
- [x] 图文笔记发布
- [x] 内置 MCP Server
- [x] 定时发布（草稿调度 + 任务管理）
- [ ] 视频笔记发布
- [ ] 数据看板（笔记表现 · 粉丝增长）
- [ ] 评论 / 私信 AI 助手
- [ ] 团队协作空间
- [ ] Mac App Store 上架

## 关键词

小红书 · xiaohongshu · xhs · redbook · Little Red Book · RED · 小红书自动化 · 小红书发布工具 · 小红书桌面客户端 · 小红书 Mac 客户端 · 小红书 MCP · MCP Server · Model Context Protocol · Claude · Cursor · Cline · AI Agent · 内容创作 · 自媒体工具 · 社交媒体管理

## 联系我们

- 官网：[redmate.app](https://redmate.app)
- 邮箱：[support@redmate.app](mailto:support@redmate.app)
- 反馈与建议：欢迎在本仓库提 [Issue](../../issues)

---

<div align="center">

**RedMate · 让 AI 接管你的小红书**

Made with 🍎 on macOS

</div>
