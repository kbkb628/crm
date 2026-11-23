# 贡献指南

感谢你愿意参与 Pi Native CRM。

## 开始之前

- 本项目以自托管方式分发：**谁在一台 VPS 上安装，谁就是用户**。任何"在开发者机器上能跑、在干净克隆里跑不起来"的改动，都算产品缺陷。
- 先读一遍 [`README.md`](README.md) 的架构与快速开始部分，确保本地环境可以启动。
- 提交前请确认 `pnpm typecheck` 与 `pnpm lint` 是干净的。

## 开发流程

```bash
git clone https://github.com/kbkb628/crm.git
cd crm
pnpm install --frozen-lockfile
cp .env.example .env.local   # 填写 Supabase / Redis / 应用地址
pnpm dev
```

分支命名建议：

```text
feat/short-slug     # 新功能
fix/short-slug      # 缺陷修复
chore/short-slug    # 依赖与配置
docs/short-slug     # 文档
```

提交信息使用 Conventional Commits，主题行祈使句、不超过 72 字符：

```text
feat: kanban fractional indexing
fix: cron 恢复卡在 sending 的消息
docs: 补充自托管升级说明
```

## 提交 PR 之前

1. 一个 PR 只做一件事，写清动机、影响面与验证方式。
2. 涉及数据库变更时，提供可重复应用的迁移文件，并说明它对已有安装的影响。
3. 涉及界面或用户流程时，附上可视化证据（截图或录制）。
4. 涉及鉴权、租户隔离、审计或数据保留时，请在描述里明确说明验证过的路径。
5. 不要提交真实客户数据、真实凭据或任何 `.env` 文件。

## 安全

安全问题不要开公开 Issue，请按 [`SECURITY.md`](SECURITY.md) 私下报告。

## 行为准则

保持专业、就事论事。技术分歧用证据说话：代码、日志、可复现步骤。
