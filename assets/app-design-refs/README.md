# Cert Master · App 设计稿参考

> ⚠️ **仅供团队对齐参考，不是开发规范**。设计师产出的 App 视觉稿，让队员看到完整的"应该长这样"。具体开发以产品 PRD 为准。

| 文件 | 内容 | 用途 |
|------|------|------|
| `01-cert-list.png` | 全部认证页 — 列表 + 顶部筛选 tabs | 列表页参考 |
| `02-design-system-overview.png` | 完整 spec sheet 全图（colors/typo/mascot/...） | 设计系统总览 — 本设计系统就是基于它做的 |
| `03-home-page.png` | 首页（未登录 + 4 大入口 + 热门考试 + Why） | 首页交互 / 信息层级 |
| `04-login-register.png` | 登录 + 注册 + 三方登录 + 新用户福利 | 注册流转化设计 |
| `05-exam-detail.png` | AWS SAA-C03 考试详情（今日进度 + 任务 + AI 建议） | 考试主功能页 |
| `06-register-flow.png` | 注册 4 步流程（创建账号 → 设置账号 → 选择目标 → 成功） | Onboarding 引导设计 |
| `07-profile.png` | 我的 / 个人中心（用户卡 + VIP + 4 stats + 鼓励 banner） | 个人中心交互 |
| `08-ai-solve.png` | AI 解题（拍照/手动/语音 输入 + AI 解析 + 选项分析） | AI 解题核心功能 |

## 使用建议

- **设计师**：看本目录为主，理解整体视觉调性
- **前端**：开发时优先用 `tokens/tokens.css` + 各 spec section（buttons / chips / cards 等），不要逐像素照搬这些图
- **PM**：用作功能讨论的视觉锚点

## 命名

`{编号}-{页面简称}.png`，编号无序号意义（按 1-6 是导入顺序）。
