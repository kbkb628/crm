# 安全策略

## 支持的版本

Pi Native CRM 从 `main` 滚动发布，安全修复只落在最新版本。自托管安装请保持更新：

```bash
bash hostgator-setup-kit/update.sh
```

| 版本 | 是否支持 |
| --- | --- |
| `main`（最新） | 是 |
| 历史快照 | 否 |

## 报告漏洞

**不要为漏洞开公开 Issue。**

请使用 GitHub 的私下漏洞报告：
<https://github.com/kbkb628/crm/security/advisories/new>

预期节奏：

- 7 天内确认收到；
- 30 天内给出评估与结论，确认后提供修复计划；
- 如果你愿意，会在发布的 advisory 中致谢。

## 关注范围

尤其希望收到以下方向的报告：

- 跨租户数据泄漏（RLS 绕过、`organization_id` 过滤缺失）
- 鉴权 / RBAC 绕过（`viewer` / `agent` / `manager` / `admin`、平台管理员）
- 个人数据暴露（LGPD）：联系人、会话、WhatsApp 媒体
- Webhook 或 `/api/v1` 的注入类问题
- 凭据泄漏：API Key、Bearer Token、会话 Cookie

自托管实例由托管方负责；服务器配置问题（防火墙、VPS 的 TLS 等）不在项目范围内，但安装套件的改进建议欢迎以普通 Issue 提出。
