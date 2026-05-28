# Contributing

欢迎参与 MarkFlow 的改进。

## 开发流程

1. Fork 仓库并创建功能分支。
2. 使用 `pnpm install` 安装依赖。
3. 使用 `pnpm desktop:dev` 启动开发环境。
4. 提交前运行必要检查。

```sh
pnpm type-check
pnpm desktop:build:web
```

## Commit 建议

推荐使用简洁的 Conventional Commits：

- `feat: add export preset`
- `fix: repair header drag region`
- `docs: update readme`
- `chore: update build config`

## Issue 建议

提交问题时请尽量包含：

- 操作系统与版本
- MarkFlow 版本
- 复现步骤
- 预期结果与实际结果
- 截图或录屏
