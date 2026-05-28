# Development Notes

## Requirements

- Node.js 22
- pnpm 11
- macOS is recommended for desktop packaging

## Useful Commands

```sh
pnpm install
pnpm web dev
pnpm desktop:dev
pnpm desktop:build:web
pnpm exec electron-builder --mac dir
```

## Desktop Output

```txt
release/mac/MarkFlow.app
```

## Notes

- The local macOS build is unsigned unless an Apple Developer ID is configured.
- Generated files under `release/`, `dist/`, `.playwright-cli/`, and `node_modules/` should not be committed.
