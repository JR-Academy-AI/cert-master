# Cert Master / 考证匠 — Design System

> 这是一个 **UI 规范 / 设计系统**，不是产品代码。
> 双击 `index.html` 就能看，不需要 npm install / 不需要 build。

---

## 目录结构

```
cert-master/
├── index.html              ← 设计系统（19+4 sections，双击打开就能看）
├── tokens/
│   ├── tokens.json         ← Design tokens 源数据（W3C 格式 / Style Dictionary 兼容）
│   └── tokens.css          ← CSS Variables（--cm-*），任何项目 import 即可用
└── assets/
    ├── logo/               ← 横版 / 紧凑 / Avatar logo
    ├── mascot/             ← 8 个企鹅状态
    ├── stickers/           ← 品牌徽章贴纸
    └── decorations/        ← 装饰素材
```

---

## 用法

### 看规范
双击 `index.html`，浏览器打开即可。19 + 4 个 section：
色彩 / 字体 / Mascot / 按钮 / 输入框 / 标签 / 开关复选 / 图标 / 导航 / 进度 / Alert / 卡片 / Modal / Dropdown / Pagination / Tooltip / Spacing / Radius / Shadow + Sticker + Do/Don't。

### 在产品里用 tokens

```css
/* 任何 CSS 文件顶部 */
@import url('path/to/cert-master/tokens/tokens.css');

.my-cta {
  background: var(--cm-yellow);
  color: var(--cm-ink);
  border-radius: var(--cm-radius-full);
  box-shadow: var(--cm-glow-yellow);
  padding: 0 var(--cm-space-6);
  height: 48px;
}
```

CSS 前缀 `--cm-*` 跟 UniMate AI 的 `--um-*` 完全隔离，可同 import 不冲突。

### 在 JS / Figma / Style Dictionary 里读

`tokens/tokens.json` 是 [W3C Design Tokens 格式](https://design-tokens.github.io/community-group/format/)：
- 喂 [Style Dictionary](https://amzn.github.io/style-dictionary/) 输出 iOS / Android / Tailwind / Sass
- 用 [Tokens Studio for Figma](https://tokens.studio/) 导入 Figma

---

## 品牌 DNA（一句话）

> **专业但有温度** — 一只戴学士帽的企鹅，陪你考过该考的证。
> Duolingo 的节奏感 × 教务系统的可信感 × 学生备考的紧迫感。

四条不可妥协：**背景灰 (`#F5F6F8`) · 考证黄 CTA · 企鹅 IP · 4pt 网格**。

跟 UniMate (牛小匠) 严格区分：**Cert Master 用企鹅，不用牛；用黄，不用 coral；用 PingFang SC，不用 Plus Jakarta Sans**。

---

## 红线（PR 看到立即打回）

- ❌ 大块页面 bg 用 `#FFFFFF`（必须 `#F5F6F8`，卡片才用白）
- ❌ 把企鹅换成牛 / 其它动物（牛是 UniMate AI 的）
- ❌ 蓝色作为主 CTA（蓝是 Info / AI 提示）
- ❌ 矩形按钮 / 小圆角扁平按钮（必须 Pill 或 12-24px 圆角）
- ❌ 自创新 mascot 表情（只用 8 标准态）
- ❌ Ant Design / MUI 默认外观未做品牌改造
- ❌ 把 PingFang SC 换成思源 / 微软雅黑作为主字体（fallback 可）

---

## Mascot 8 个标准态

| State | 中文 | 场景 |
|-------|------|------|
| happy | 开心 | 完成任务 / 获得奖励 |
| studying | 学习中 | 默认 / 课程进行中 |
| thinking | 思考中 | 空状态 / 答题暂停 |
| ai-analyzing | AI 分析中 | AI 解析 / loading |
| sprint | 冲刺 | 倒计时 / streak |
| anxious | 焦虑 | 错题多 / 考前压力 |
| passed | 通过啦 | 证书拿到 / 解锁 |
| champion | 满分拿下 | 100 分 / 全通过 |

新场景必须 map 到已有 8 态，**禁止自创**。

---

## 待补 (TODO)

- [ ] Logo 3 件套落盘（`assets/logo/horizontal.png` / `compact.png` / `avatar.png`）
- [ ] 8 个差异化 Mascot 落盘（替换 §03 占位 emoji）
- [ ] 4 张卡片配图落盘（`assets/cards/{study-plan,mock-exam,notes,wrong-book}.png`）
- [ ] Style Dictionary 配置，自动导出 Tailwind preset / iOS Swift / Android XML
- [ ] 等 Cert Master 产品立项后，token 文件做软链 / npm 包发布

---

## Deploy

GitHub Pages auto-deploy via `.github/workflows/deploy.yml` — push 到 `main` 自动构建并发布。

---

## 维护

- 源 spec 图：`assets/mascot/spec-sheet.png`（ChatGPT 2026-05-11）
- 最近更新：2026-05-11
- 任何 token 改动必须三处同步：`tokens.json` / `tokens.css` /（如果以后加）`tokens.ts`。
