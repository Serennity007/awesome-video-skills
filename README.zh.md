[English](README.md) | [中文](README.zh.md) | [日本語](README.ja.md) | [Français](README.fr.md) | [Español](README.es.md) | [العربية](README.ar.md) | [한국어](README.ko.md) | [Português](README.pt.md) | [Русский](README.ru.md) | [Deutsch](README.de.md)
<div align="center">

<img src=".banner.svg" width="100%" alt="banner">

</div>


# 🎬 Awesome Video Skills — 中文版

> 别再谷歌 FFmpeg 命令了。把技能写一次，让 AI 永远帮你剪视频。

<div align="center">

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Skills](https://img.shields.io/badge/skills-11-blueviolet)](#全部技能)

</div>

---



## 问题

你每次做项目都要花**大量时间**搜索 FFmpeg 参数、查 DaVinci Resolve 快捷键、重写同样的字幕脚本。你的 AI 助手不知道你的工作流、你的预设、你的偏好。

## 解决方案

把你的视频编辑知识写成 **AI 技能**，只需写一次。你的 AI 助手读取技能后，能生成完全正确的流水线、预设或脚本 — 每次都是。

<div align="center">

| ❌ 没有技能 | ✅ 拥有技能 |
|:---:|:---:|
| 花 30 分钟搜索 FFmpeg 参数 | “把这个视频压缩成适合 YouTube 的版本” → 完美命令 |
| 手动为 5 个平台调整尺寸 | 一键批量导出所有平台 |
| 反复重写字幕脚本 | AI 直接生成你想要的 Whisper 流水线 |
| 拍脑袋猜 YouTube SEO | 结构化的标题/描述/标签优化 |

</div>

---

## 全部技能

### 视频剪辑 (Video Editing)

| 技能 | 说明 | 文件 |
|-------|-------------|------|
| 🎥 FFmpeg Master | 剪切、合并、转换、压缩 — 完整 FFmpeg 流水线自动化 | [`skills/视频剪辑/ffmpeg-master.md`](skills/视频剪辑/ffmpeg-master.md) |
| 🤖 OrkasVideoStudio | 智能体驱动的视频制作，使用可编辑的 `plan.json` 时间线 | [`skills/视频剪辑/orkas-videostudio.md`](skills/视频剪辑/orkas-videostudio.md) |
| 🎨 DaVinci Resolve | 调色、Fusion 特效、Fairlight 音频、输出预设 | [`skills/视频剪辑/davinci-resolve.md`](skills/视频剪辑/davinci-resolve.md) |
| 🎬 Premiere Pro | 序列设置、导出预设、Dynamic Link、Essential Graphics | [`skills/视频剪辑/premiere-pro.md`](skills/视频剪辑/premiere-pro.md) |

### 特效制作 (Effects)

| 技能 | 说明 | 文件 |
|-------|-------------|------|
| ✨ Motion Graphics | After Effects 表达式、CSS 动画、Lottie 模板 | [`skills/特效制作/motion-graphics.md`](skills/特效制作/motion-graphics.md) |
| 🤖 AI Video Generation | Runway、Pika、Sora 提示词工程与后期处理 | [`skills/特效制作/ai-video-generation.md`](skills/特效制作/ai-video-generation.md) |

### 字幕处理 (Subtitles)

| 技能 | 说明 | 文件 |
|-------|-------------|------|
| 📝 Subtitle Generation | Whisper 转录、SRT/ASS 格式、字幕烧录 | [`skills/字幕处理/subtitle-generation.md`](skills/字幕处理/subtitle-generation.md) |
| 🌐 Translation Subtitles | 多语言字幕流水线、双语字幕、质量检查 | [`skills/字幕处理/translation-subtitles.md`](skills/字幕处理/translation-subtitles.md) |

### 音频处理 (Audio)

| 技能 | 说明 | 文件 |
|-------|-------------|------|
| 🎵 Audio Mixing | 降噪、EQ、压缩、标准化、背景音乐混音 | [`skills/音频处理/audio-mixing.md`](skills/音频处理/audio-mixing.md) |

### 发布优化 (Publishing)

| 技能 | 说明 | 文件 |
|-------|-------------|------|
| 📈 YouTube Optimization | SEO 标题、缩略图设计、标签、分析、发布排期 | [`skills/发布优化/youtube-optimization.md`](skills/发布优化/youtube-optimization.md) |
| 🌍 Multi-Platform Publish | YouTube、TikTok、Bilibili、Instagram — 规格、批量导出、自动化 | [`skills/发布优化/multi-platform-publish.md`](skills/发布优化/multi-platform-publish.md) |

---

## 快速开始

### Cursor

把任意技能文件复制到项目的 `.cursorrules` 或 `.cursor/rules/` 目录：

```bash
cp skills/视频剪辑/ffmpeg-master.md .cursor/rules/ffmpeg.md
```

或者引用多个技能：

```bash
mkdir -p .cursor/rules
cp skills/**/*.md .cursor/rules/
```

### Claude Code

在 `CLAUDE.md` 中添加技能作为项目上下文：

```markdown
## Video Skills
- @skills/视频剪辑/ffmpeg-master.md
- @skills/字幕处理/subtitle-generation.md
```

### Kimi Code

把技能文件复制到项目根目录或 `.kimi/` 目录：

```bash
mkdir -p .kimi/skills
cp skills/**/*.md .kimi/skills/
```

### 使用技能

安装完成后，只需自然地询问你的 AI 助手：

```
"把这个视频压缩到 50MB 以内，方便邮件发送"
"给这个访谈视频生成中文字幕"
"把我的 YouTube 视频做成抖音版本"
"优化我 YouTube 视频的标题和描述，做好 SEO"
"在旁白下面混入背景音乐，音量压到 -18dB"
```

---

## 参与贡献

欢迎提交新的视频技能！详见 [CONTRIBUTING.md](CONTRIBUTING.md)。

快速参与方式：
1. Fork 本仓库
2. 在 `skills/` 下合适的分类中添加你的技能
3. 遵循技能模板格式（适用场景、Instructions、Templates、Pitfalls）
4. 提交 PR

---

## 相关项目

- [awesome-skills](https://github.com/liangzhengtao/awesome-skills) — 各领域 AI 技能精选合集
- [awesome-ai-rules](https://github.com/liangzhengtao/awesome-ai-rules) — AI 编程助手规则配置
- [vibe-check](https://github.com/liangzhengtao/vibe-check) — AI 技能质量验证工具
- [commit-ai](https://github.com/Serennity007/ai-commit) — AI 驱动的 Git 提交信息生成
- [awesome-mcp-servers](https://github.com/liangzhengtao/awesome-mcp-servers) — MCP 服务器合集

---

## 许可证

[MIT](LICENSE) © [liangzhengtao](https://github.com/Serennity007)

---
