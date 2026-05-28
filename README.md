# MarkFlow

---

[English](#features) · [中文介绍](#中文介绍)

---

<p align="center">
  <img src="./apps/web/src/assets/images/markflow-icon.png" width="112" alt="MarkFlow icon" />
</p>

MarkFlow is a desktop Markdown formatting workspace for writing, previewing, styling, copying, and exporting long-form content.

It is designed for creators, technical writers, and content operators who prefer writing in Markdown but still need polished output for publishing platforms, blogs, documentation pages, PDFs, or image-based sharing.

## Features

- Write Markdown with a split editor and live preview
- Manage local articles with autosave
- Adjust themes, typography, colors, and code block styles
- Insert common content blocks such as images, formulas, and tables
- Copy formatted HTML for content platforms
- Export Markdown, styled HTML, plain HTML, PDF, and PNG
- Use AI assistant and text-to-image entry points from the top toolbar
- Run as a macOS desktop app powered by Electron

## Use Cases

- Formatting WeChat Official Account articles and self-media posts
- Writing technical blogs, tutorials, and knowledge-sharing articles
- Preparing project notes, release notes, and product explainers
- Turning Markdown drafts into HTML, PDF, or PNG deliverables
- Creating clean long-form content before publishing it to different platforms

## Development

Recommended environment: Node.js 22 and pnpm.

```sh
pnpm install
pnpm web dev
pnpm desktop:dev
```

## Build

```sh
pnpm desktop:build:web
pnpm exec electron-builder --mac dir
```

The macOS app will be generated at:

```txt
release/mac/MarkFlow.app
```

If no Apple Developer ID is configured locally, electron-builder will skip macOS code signing. This is fine for local development and demos, but signing and notarization are recommended before public distribution.

## Project Structure

```text
markflow/
  apps/web/              Main Vue application
  desktop/electron/      Electron desktop entry
  desktop/assets/        Desktop icon assets
  branding/icons/        Product icon drafts
  packages/              Markdown rendering and shared packages
  docs/                  Development notes
```

## 中文介绍

MarkFlow 是一个桌面端 Markdown 内容排版工作台，用来完成长内容的写作、预览、样式调整、HTML 复制和多格式导出。

它适合已经习惯用 Markdown 写作，但发布前还需要处理排版、样式和导出格式的内容创作者、技术写作者和内容运营者。你可以把它当作内容从草稿到发布前的整理工作台。

### 主要功能

- Markdown 编辑与实时预览
- 本地文章管理与自动保存
- 主题、字号、颜色、代码块样式调整
- 插入图片、公式、表格等常用内容
- 复制排版后的 HTML 内容
- 导出 Markdown、带样式 HTML、无样式 HTML、PDF、PNG
- 顶部工具栏内置 AI 助手和文生图入口
- 基于 Electron 的 macOS 桌面端体验

### 适合场景

- 公众号文章和自媒体长文排版
- 技术博客、教程和知识分享文章写作
- 项目说明、版本说明和产品介绍整理
- 将 Markdown 草稿转换为 HTML、PDF 或 PNG 文件
- 在发布到不同内容平台前统一检查和调整样式

### 本地开发

建议使用 Node.js 22 和 pnpm。

```sh
pnpm install
pnpm web dev
pnpm desktop:dev
```

### 构建桌面端

```sh
pnpm desktop:build:web
pnpm exec electron-builder --mac dir
```

打包完成后会生成：

```txt
release/mac/MarkFlow.app
```

本地未配置 Apple Developer ID 时，electron-builder 会跳过 macOS 签名。这不影响本机开发和演示，但正式分发前建议配置签名与公证。

### 项目结构

```text
markflow/
  apps/web/              MarkFlow 主应用
  desktop/electron/      Electron 桌面端入口
  desktop/assets/        桌面端图标资源
  branding/icons/        产品图标设计稿
  packages/              Markdown 渲染与共享工具包
  docs/                  开发说明
```
