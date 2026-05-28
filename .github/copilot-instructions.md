# Copilot Instructions

This repository contains MarkFlow, a pnpm monorepo for a Vue 3 Markdown editor and Electron desktop app.

## Commands

- Install dependencies: `pnpm install`
- Start web app: `pnpm web dev`
- Start desktop dev mode: `pnpm desktop:dev`
- Type check: `pnpm type-check`
- Build web app for desktop: `pnpm desktop:build:web`
- Package macOS app directory: `pnpm exec electron-builder --mac dir`

## Structure

- `apps/web`: Main Vue 3 application
- `desktop/electron`: Electron main process
- `desktop/assets`: Desktop app assets
- `packages/core`: Markdown rendering logic
- `packages/shared`: Shared editor utilities and configuration
- `branding/icons`: MarkFlow icon source files and iterations

## Style

- Prefer existing Vue Composition API and Pinia patterns.
- Keep changes focused and avoid broad refactors.
- Use existing UI components in `apps/web/src/components/ui`.
- Keep MarkFlow product naming consistent in user-facing text.
