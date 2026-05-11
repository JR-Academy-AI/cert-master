# Cert Master / 考证匠 — Design System

> **完整设计规范文档**。目标读者：Claude / 设计师 / 前端 / 内容运营。
> 任何关于「该用什么色、什么字、什么 mascot、什么按钮」的问题，先来这里查。
>
> 配套文件：
> - `index.html` — 视觉品牌手册（双击就能看）
> - `tokens/tokens.json` — W3C Design Tokens 源数据
> - `tokens/tokens.css` — `--cm-*` CSS 变量
> - `README.md` — 仓库使用说明
>
> Last updated: 2026-05-11 · v0.2

---

## 目录

1. [品牌定位](#1-品牌定位)
2. [品牌 DNA](#2-品牌-dna)
3. [Mascot 系统](#3-mascot-系统)
4. [Color 系统](#4-color-系统)
5. [Typography 系统](#5-typography-系统)
6. [Spacing · Radius · Shadow](#6-spacing--radius--shadow)
7. [Logo & Banner](#7-logo--banner)
8. [组件规范](#8-组件规范)
9. [Voice & Tone](#9-voice--tone)
10. [Motion](#10-motion)
11. [Do / Don't 红线](#11-do--dont-红线)
12. [Asset 目录映射](#12-asset-目录映射)
13. [跟 UniMate AI 的隔离规则](#13-跟-unimate-ai-的隔离规则)

---

## 1. 品牌定位

**Cert Master / 考证匠** — 全球华人考证人的 AI 学习搭子。

| 维度 | 内容 |
|------|------|
| **一句话** | 你的 AI 考证搭子，学习更高效 |
| **English** | Your AI Study Buddy, Learn Smarter. |
| **场景** | 注会 / 税务师 / 一建 / 法考 / 教师资格证 / IT 认证 …… 任何"题量大、周期长、压力大"的考证场景 |
| **目标用户** | 在职备考人 + 应届考证 + 国外考本地证 (CPA AU / RG146 …) 的华人 |
| **竞品对标** | 粉笔 / 高顿 (传统题库) · Duolingo (游戏化) · ChatGPT (通用 AI) |
| **核心差异** | **AI 全程陪练** + **错题智能整理** + **个性化学习计划** + **企鹅 IP 陪伴感** |
| **母品牌** | JR Academy (匠人学院) — 跟 UniMate AI / SigmaQ / JR Jobs 同属一家 |

**不做什么**：
- 不做万能搜索引擎（不抢 ChatGPT 的活）
- 不做纯题库（不抢粉笔的活）
- 不做"刷分代练"（违反考试公平）
- 不做线下面授（线上 AI 是核心）

---

## 2. 品牌 DNA

### 一句话
**专业但有温度** — 一只戴学士帽的企鹅，陪你考过该考的证。

### 三圈混合
- **Duolingo 的节奏感** — streak / 完课庆祝 / 弱点强化
- **教务系统的可信感** — 知识图谱 / 章节进度 / 通过率统计
- **学生备考的紧迫感** — 倒计时 / 冲刺 / "再不学就来不及了"

### 四条不可妥协（看到就打回）

| 铁律 | Why |
|------|-----|
| **背景灰 `#F5F6F8`** 做大块页面 bg，**白色**只用于卡片表面 | 纯白 `#FFFFFF` 显得冷、像 SaaS 后台、没温度 |
| **考证黄 `#FFC52A`** 做主 CTA，绝不蓝色 | 蓝 = OpenAI / SaaS 味，跟 Cert Master 学生气质冲突 |
| **企鹅** 做 mascot，绝不换其它动物 | 企鹅是品牌资产，跟 UniMate (牛) 严格区分 |
| **4pt 网格**做所有 spacing | 跟 PingFang SC 字号严丝合缝，避免半像素 |

### 跟其它学习品牌的差别

| 品牌 | 主色 | Mascot | 调性 |
|------|------|--------|------|
| Duolingo | 绿 | 猫头鹰 | 病态游戏化 |
| Brilliant | 深蓝 | 无 | 硬核智识 |
| 粉笔 | 红 | 无 | 国内题库快餐 |
| 高顿 | 蓝 | 无 | 严肃学术派 |
| **Cert Master** | **黄** | **企鹅** | **专业 + 暖心 + 学生气** |

---

## 3. Mascot 系统

### 3.1 IP 设定

**圆胖企鹅** · 学士帽（毕业生气质） · 黄喙（呼应主色） · 大眼睛圆脸 · 单一立绘风格（黑白主体 + 黄色点缀）。

### 3.2 8 个标准态（禁止自创）

| State | 中文名 | 视觉特征 | 触发场景 | 文件 |
|-------|--------|---------|---------|------|
| `happy` | 开心 | 学士帽 + 双手举起 + 眯眼笑 + 黄领结 | 完成任务 / 获得奖励 / 抽中卡 | `assets/mascot/happy.png` |
| `studying` | 学习中 | 戴耳机 + 圆框眼镜 + 笔记本电脑 + 咖啡 | 默认页面 / 课程进行中 / 题目作答 | `assets/mascot/studying.png` |
| `thinking` | 思考中 | 圆框眼镜 + 手托腮 + 头顶问号 | 空状态 / 答题暂停 / 「还没想到？」 | `assets/mascot/thinking.png` |
| `ai-analyzing` | AI 分析中 | 学士帽 + 放大镜 + 蓝色透明数据屏 | AI 解析 loading / 出报告中 / 智能匹配 | `assets/mascot/ai-analyzing.png` |
| `sprint` | 冲刺 | 学士帽 + 怒眼 + 火焰 + 跑步姿势 | 考前倒计时 / 7 天冲刺 / streak ≥7 天 | `assets/mascot/sprint.png` |
| `anxious` | 焦虑 | 红头巾 + 笔记本 + 汗滴 + 沮丧眼 | 错题率高 / 考前 3 天没复习 / 弱点提醒 | `assets/mascot/anxious.png` |
| `passed` | 通过啦 | 学士帽 + 毕业证卷轴 + 眨眼欢呼 | 章节通过 / 模考及格 / 拿到证书 | `assets/mascot/passed.png` |
| `champion` | 满分拿下 | 皇冠 + 披风 + 金牌 + 星星 | 100 分 / 全章节满分 / 排行榜第一 | `assets/mascot/champion.png` |

### 3.3 选择决策树

```
用户做了什么？
├── 完成（通过/解锁/奖励）
│   ├── 普通完成 → happy
│   ├── 章节/模考通过 → passed
│   └── 满分/榜首 → champion
│
├── 进行中
│   ├── 默认进行中 → studying
│   ├── AI 在算 / loading → ai-analyzing
│   └── 倒计时/冲刺/streak → sprint
│
├── 卡住 / 出错
│   ├── 用户没动作（空状态） → thinking
│   └── 错题多/快没时间 → anxious
│
└── 不知道用哪个 → studying（默认）
```

### 3.4 3D 旗舰形象（hero / 品宣专用）

| State | 用途 | 文件 |
|-------|------|------|
| `happy 3D` | App 启动屏 / 公众号封面 / 开屏挥手 | `assets/mascot-3d/happy.png` |
| `thinking 3D` | 空状态大版 / 默认头像 / loading 大图 | `assets/mascot-3d/thinking.png` |
| `certified 3D` | 通过页 / 证书页 / 案例展示 / 转化页 | `assets/mascot-3d/certified.png` |

**3D 版只用作主视觉**，不要塞进按钮 / chip / toggle 等小尺寸 UI（小尺寸用 §3.2 扁平版）。

### 3.5 Mascot 用尺寸 & 工具类

| 尺寸 | 用途 | CSS class |
|------|------|-----------|
| 14-18px | chip 内嵌 / 行内小图标 | `.peng .peng-14` ~ `.peng-18` |
| 22-32px | 按钮 / toggle knob / nav brand / 进度 tracker | `.peng-22` ~ `.peng-32` |
| 44-64px | banner header logo / 卡片 thumbnail | `.peng-44` |
| 100-200px | mascot 单元格 / hero / modal 主形象 | 直接用 `<img>` |

源文件：`assets/logo/avatar-icon.png`（96×96 缩图）— 用于所有小尺寸场景。

### 3.6 红线

- ❌ 不要自创新表情（如 "睡觉企鹅" / "结婚企鹅"）— 新场景必须 map 到已有 8 态
- ❌ 不要把企鹅换成其它动物（牛是 UniMate 的，不要混）
- ❌ 不要给企鹅改色（白肚不能变粉，黑背不能变蓝）
- ❌ 不要拉伸 / 压扁 / 倾斜（保持原始比例）
- ❌ 一屏 ≥ 2 个不同状态的 mascot（视觉太乱）

---

## 4. Color 系统

### 4.1 品牌色 / Brand (5)

| 名称 | Hex | CSS Var | 角色 |
|------|-----|---------|------|
| 考证黄 | `#FFC52A` | `--cm-yellow` | **Primary** · CTA · 能量 / 通过 |
| 活力橙 | `#FF7A45` | `--cm-orange` | Streak · 高频 · 紧迫 / Danger |
| 薄荷绿 | `#2ECCB2` | `--cm-mint`   | Success · 完成 · 通过 |
| 天空蓝 | `#5AA7FF` | `--cm-sky`    | Info · AI 提示 · loading |
| 香芋紫 | `#A78BFA` | `--cm-taro`   | Premium · 进阶 · VIP 标识 |

### 4.2 中性色 / Neutral (7)

| 名称 | Hex | CSS Var | 用途 |
|------|-----|---------|------|
| 深黑 | `#111827` | `--cm-ink` | H1 / 高亮正文 |
| 深灰 | `#374151` | `--cm-graphite` | 次正文 |
| 中灰 | `#6B7280` | `--cm-slate` | Caption / 副标 |
| 浅灰 | `#9CA3AF` | `--cm-mist` | Placeholder / disabled label |
| 更浅灰 | `#E5E7EB` | `--cm-fog` | Border / divider |
| 背景灰 | `#F5F6F8` | `--cm-canvas` | **页面默认 bg**（不要纯白） |
| 白色 | `#FFFFFF` | `--cm-white` | 卡片表面 |

### 4.3 Wash（10% 浅色，chip / alert bg）

| 名称 | Hex | CSS Var |
|------|-----|---------|
| 黄洗 | `#FFF7DA` | `--cm-wash-yellow` |
| 橙洗 | `#FFE5D9` | `--cm-wash-orange` |
| 绿洗 | `#DAF5EF` | `--cm-wash-mint` |
| 蓝洗 | `#DCE9FF` | `--cm-wash-sky` |
| 紫洗 | `#ECE4FE` | `--cm-wash-taro` |

### 4.4 Semantic alias

| 用途 | 等于 |
|------|------|
| `--cm-success` | `--cm-mint` |
| `--cm-warning` | `--cm-yellow` |
| `--cm-danger`  | `--cm-orange` |
| `--cm-info`    | `--cm-sky` |

### 4.5 用色决策树

```
要表达什么？
├── 主 CTA / 默认动作 → 考证黄 (#FFC52A)
├── 完成 / 通过 / 已答对 → 薄荷绿 (#2ECCB2)
├── 错题 / 警告 / 倒计时 → 活力橙 (#FF7A45)
├── AI 提示 / Info / loading → 天空蓝 (#5AA7FF)
├── VIP / 进阶 / 课程 → 香芋紫 (#A78BFA)
├── 中性正文 / 卡片 / 边框 → Neutral 七档
└── chip / alert 浅底 → Wash 五档
```

### 4.6 红线

- ❌ 不要把蓝 (`#5AA7FF`) 当主 CTA
- ❌ 不要在一屏堆 ≥3 种品牌色 CTA（视觉过载）
- ❌ 大块页面 bg 不要纯白
- ❌ 不要给文字加阴影 / glow（除非是 deadline / 错题等强调场景，用 wash 底就够）

---

## 5. Typography 系统

### 5.1 字体族

| 角色 | 字体 | CSS Var |
|------|------|---------|
| 主字体 | `'PingFang SC', 'Hiragino Sans GB', 'Microsoft YaHei', system-ui, ...` | `--cm-font-sans` |
| 等宽 | `'JetBrains Mono', 'SF Mono', 'Cascadia Code', Menlo, ...` | `--cm-font-mono` |

**等宽专用场景**：题号 / 分数 / 计时器 / 答题代码 / hex 值。

### 5.2 字号尺度

| Level | Size | Weight | Letter-spacing | CSS class |
|-------|------|--------|----------------|-----------|
| H1 | 34px | Bold (700) | -1% | `.cm-h1` |
| H2 | 24px | Semibold (600) | -0.5% | `.cm-h2` |
| H3 | 20px | Semibold (600) | 0 | `.cm-h3` |
| Body | 16px | Regular (400) | 0 | `.cm-body` |
| Caption | 12px | Regular (400) | 0 | `.cm-caption` |

### 5.3 行高

| 用途 | line-height | CSS Var |
|------|-------------|---------|
| 标题 (H1-H3) | 1.25 | `--cm-lh-heading` |
| 正文 | 1.6 | `--cm-lh-body` |

### 5.4 红线

- ❌ 不要把 PingFang SC 换成思源黑体 / 微软雅黑作为主字体（fallback 可）
- ❌ 不要在正文里用 `font-weight: 400` 以下（细字在中文里发虚）
- ❌ 不要在标题里同时用多个 weight（一个层级一个 weight）
- ❌ 不要在 body 16px 以下做大段中文（移动端不舒服）

---

## 6. Spacing · Radius · Shadow

### 6.1 Spacing — 4pt 网格

```
4 / 8 / 12 / 16 / 24 / 32 / 48 / 64
```

| 用途 | 推荐 |
|------|------|
| 内联元素 gap (chip / icon) | 4-8px |
| 表单内 padding | 12-16px |
| 卡片 padding | 16-24px |
| Section 之间 | 24-32px |
| 页面顶/底 padding | 48-64px |

CSS Var：`--cm-space-1` ~ `--cm-space-16`（数字 = px / 4）。

### 6.2 Radius

| 名称 | px | CSS Var | 用途 |
|------|-----|---------|------|
| xs | 4 | `--cm-radius-xs` | 小 tag / inline code |
| sm | 8 | `--cm-radius-sm` | 输入框 / 小按钮 |
| md | 12 | `--cm-radius-md` | 卡片小块 / chip |
| lg | 16 | `--cm-radius-lg` | 大卡片 / modal |
| xl | 24 | `--cm-radius-xl` | hero banner / 顶部大块 |
| full | 9999 | `--cm-radius-full` | Pill 按钮 / chip / avatar |

**默认偏好**：所有按钮用 `full` 胶囊，避免矩形按钮。

### 6.3 Shadow

| 名称 | 值 | 用途 |
|------|-----|------|
| sm | `0 1px 2px rgba(0,0,0,0.04)` | 静态卡片 / divider 替代 |
| md | `0 4px 12px rgba(0,0,0,0.08)` | hover 卡片 / 浮起元素 |
| lg | `0 10px 24px rgba(0,0,0,0.10)` | Modal / floating panel |
| **glow-yellow** | `0 8px 20px rgba(255,197,42,0.35)` | Primary CTA 默认发光 |
| glow-mint | `0 8px 20px rgba(46,204,178,0.30)` | 通过 / 完成发光 |
| glow-sky | `0 8px 20px rgba(90,167,255,0.30)` | AI 提示发光 |

---

## 7. Logo & Banner

### 7.1 Logo 三件套

| 名称 | 文件 | 用途 |
|------|------|------|
| Horizontal | `assets/logo/horizontal.png` | 官网 header / 邮件签名 / 横向窄区域 / 小 banner |
| Compact | `assets/logo/compact.png` | 海报 / PPT 封面 / App 启动屏 |
| Avatar | `assets/logo/avatar.png` | App 图标位 / 头像 / 收藏卡 |
| App Icon iOS | `assets/logo/app-icon-ios.png` | iOS App Store 圆角方块图标 |
| Avatar Icon | `assets/logo/avatar-icon.png` | 96px 缩图 — 通用小企鹅头（替代 🐧 emoji） |

### 7.2 Banner 三档

| 变体 | 文件 / 实现 | 场景 |
|------|------------|------|
| **Dark Hero** | `assets/banners/hero-dark.png` | App 启动屏 / 公众号封面 / 社交卡 / 开屏 |
| **Light Banner** | `horizontal.png` + 白底卡 | 页眉 / Section header / 邮件签名 / 内文小条 |
| **Dark Strip** | `--cm-ink` 黑底 + avatar.png 圆头 + 文字 | 深色页面 footer / 课程证书页眉 |

详见 `index.html` §00 Banner 应用 sub-block。

### 7.3 净空规则

Logo 四周必须留出 **≥ 企鹅头宽度的 1/4** 作为安全边距，绝不允许任何元素侵入。

### 7.4 Logo 红线

- ❌ 不要拉伸 / 倾斜 logo
- ❌ 不要改企鹅 fill 颜色（黑就是黑，白就是白）
- ❌ 不要给 logo 加 box-shadow / glow（保持平面感）
- ❌ 不要放在低对比度 bg 上（#FFC52A 上放 horizontal logo 会糊）
- ❌ 不要把 logo 当装饰反复重复

---

## 8. 组件规范

### 8.1 Buttons — 双色拼接 Pill

所有主按钮采用 **左半文字 + 右半 action chip + 箭头** 的双色拼接结构。

| 类型 | 左半 bg | 右半 act | text color |
|------|---------|----------|-----------|
| **Primary** | `--cm-yellow` | `rgba(0,0,0,0.10)` | `--cm-ink` |
| **Hover**   | `#FFB800` (深黄) + outline ring | `rgba(0,0,0,0.18)` | `--cm-ink` |
| **Secondary** | `--cm-white` + 1.5px fog 描边 | `--cm-canvas` + 同色分割线 | `--cm-ink` |
| **Ghost** | 透明 | 无（文字 + 箭头一行） | `--cm-graphite` |

- 高度：48px
- 圆角：`full`
- 字重：700
- Glow：Primary / Hover 必带 yellow glow shadow

### 8.2 Inputs — 4 状态

| 状态 | 边框 | 背景 | 用法 |
|------|------|------|------|
| Default | 1.5px `--cm-fog` | `--cm-white` | 默认 |
| Focus | 1.5px `--cm-yellow` + 4px yellow ring (18% alpha) | `--cm-white` | 聚焦 |
| Filled | 1.5px `--cm-fog` | `--cm-canvas` | 已填写 |
| Error | 1.5px `--cm-orange` | `--cm-wash-orange` | 错误 |

- 字号：16px (避免 iOS 自动放大)
- 圆角：`sm` (8px)
- padding：`12px 16px`

### 8.3 Chips & Tags — 三组

| 类型 | 结构 | 用途 |
|------|------|------|
| **Category** | 浅 wash 底 + 26px **白色圆形** 包裹小图标 + 文字 | 类别（AI 助手 / Lecture / Quiz / Assignment） |
| **Status** | 浅 wash 底 + 8px 同色实心点 + 文字 | 状态（已完成 / 进行中 / 重点 / 热门） |
| **Outline** | 白底 + 1.5px fog 描边 + 文字 (`+ 自定义` 用 dashed) | 自定义标签 |

### 8.4 Toggle / Check / Radio

| 组件 | 关闭态 | 开启态 |
|------|--------|--------|
| Toggle | `--cm-fog` 底 + 白色 26px knob | `--cm-yellow` 底 + 26px knob 含小企鹅头 |
| Checkbox | 白底 + 2px fog 边 | `--cm-yellow` 底 + 黑 ✓ |
| Radio | 白底 + 2px fog 边 | 2px yellow 边 + 10px yellow 实心圆 |

### 8.5 Cards — 上图下文

```
┌─────────────────┐
│ 彩色渐变 wash    │ ← 180px，企鹅插图 92% 占满
│   [PENGUIN]      │
└─────────────────┘    ← 黄色 44px 圆 → 按钮飘出 (top:-22px right:16px)
│ 标题             │
│ 副标             │
└─────────────────┘
```

**4 张默认卡映射**：

| 卡 | wash | 插图 |
|---|------|------|
| 错题本 | `--cm-wash-orange` | `assets/cards/wrong-book.png` |
| 模拟考试 | `--cm-wash-mint` | `assets/cards/mock-exam.png` |
| 学习计划 | `--cm-wash-yellow` | `assets/cards/study-plan.png` |
| 章节练习 | `--cm-wash-taro` | `assets/cards/chapter-quiz.png` |

### 8.6 Alerts — 4 种

| 类型 | bg | icon-wrap |
|------|-----|-----------|
| Success | `--cm-wash-mint` | `--cm-mint` 圆 + 白 ✓ |
| Warning | `--cm-wash-yellow` | `--cm-yellow` 圆 + 黑 ! |
| Danger | `--cm-wash-orange` | `--cm-orange` 圆 + 白 × |
| Info | `--cm-wash-sky` | `--cm-sky` 圆 + 白 i |

### 8.7 Progress — 黄色斜条纹

```css
background:
  repeating-linear-gradient(-45deg, rgba(255,255,255,0.28) 0 8px, transparent 8px 16px),
  var(--cm-yellow);
animation: stripe-march 1.6s linear infinite;
```

进度条上方浮 44px 圆形 tracker，里面装 32px 小企鹅头。

### 8.8 Steps — 5 步

每步：36px 圆球 + 标题。已完成 = 黄底；进行中 = 黄底 + glow；未到 = canvas 底。step-bar 已完成段变黄。

### 8.9 Modal

`max-width: 380px` · `radius: lg` · `padding: 28px` · `shadow: lg` · 顶部 dashed 上传区。

### 8.10 Dropdown / Pagination / Tooltip

详见 `index.html` 对应 section。

---

## 9. Voice & Tone

### 9.1 整体调性

**像高年级学长** — 比你早考过这个证，能用人话说清楚，偶尔皮一下，不端架子。

### 9.2 文案规则

| ✅ 这样写 | ❌ 不要这样 |
|----------|-----------|
| 还有 12 道错题没整理 | 您还有 12 道错题待整理 |
| 这章 80% 同学都会卡在这 | 本章节为高难度知识点 |
| 拿下！+50 经验 | 恭喜您完成本次学习 |
| 再撑 7 天就考试了 | 距离考试还有 7 天 |
| AI 帮你扒了 3 个高频考点 | 系统已为您智能识别相关考点 |

### 9.3 永远别用

- "您" — 用"你"，距离感太重
- "亲" — 太微商
- "宝子 / 家人们" — 太抖音
- "强烈推荐 / 不容错过" — 营销废话
- "智能化 / 数字化 / 赋能" — 政府报告味

### 9.4 不同场景的语气

| 场景 | 范例 |
|------|------|
| 默认引导 | "开始学习" / "继续上次的进度" |
| 完成奖励 | "拿下！+50 经验" / "本章 100% 通过" |
| 错题提示 | "这题昨天也错过 — AI 来给你拆下" |
| 焦虑安抚 | "12 天还来得及，咱重点突破弱项" |
| 倒计时 | "考前 7 天 · 锁定每天 30 分钟" |
| 报错 | "网络抽了 — 点这里重试" |
| 成就 | "拿下了 100 分！截图发朋友圈？" |

---

## 10. Motion

### 10.1 Duration

| 名称 | 值 | 用途 |
|------|-----|------|
| fast | 120ms | 微交互（hover / focus） |
| base | 200ms | 状态切换（按钮按下 / toggle） |
| slow | 320ms | 页面/卡片大动效 |

### 10.2 Easing

| 名称 | 值 | 用途 |
|------|-----|------|
| standard | `cubic-bezier(0.2, 0.8, 0.2, 1)` | 默认所有缓动 |
| spring | `cubic-bezier(0.34, 1.56, 0.64, 1)` | 弹跳（checkbox 打勾 / passed 庆祝） |

### 10.3 关键动效

- **按钮 hover**：`translateY(-1px)` + 加深 glow
- **卡片 hover**：`translateY(-2px)` + shadow sm → md
- **进度条**：`stripe-march` 1.6s linear infinite — 黄色斜条纹左滑
- **完成弹窗**：spring easing 弹入
- **mascot 入场**：fade + 微 scale (0.95 → 1)

### 10.4 红线

- ❌ 不要 ≥1s 的动画（用户没耐心）
- ❌ 不要全屏视觉爆炸（保持克制）
- ❌ 不要让 mascot 持续抖动 / 旋转（除非是 sprint 状态的火焰拖尾）

---

## 11. Do / Don't 红线

### 11.1 视觉

| ✅ Do | ❌ Don't |
|-------|---------|
| 页面 bg = `--cm-canvas` (#F5F6F8)，卡片 = 白 | 页面 bg = `#FFFFFF` |
| 主 CTA = 考证黄胶囊 + 双色拼接 | 蓝色矩形按钮 |
| Mascot 用 8 标准态 | 自创新表情（睡觉 / 结婚企鹅） |
| 一屏 ≤2 个 mascot | 满屏 mascot 复读 |
| 一屏 ≤2 种品牌色作 CTA | 一屏 5 色 CTA 全堆 |
| Pill 圆角或 12-24px | 矩形 / 小圆角扁平按钮 |

### 11.2 字体

| ✅ Do | ❌ Don't |
|-------|---------|
| PingFang SC 主字 | 思源黑体 / 微软雅黑做主字 |
| Body ≥ 16px | 中文正文 < 14px |
| 标题用 -0.5% ~ -1% tracking | 标题用 +letter-spacing |
| 题号 / 分数 用 JetBrains Mono | 数字也用 PingFang |

### 11.3 文案

| ✅ Do | ❌ Don't |
|-------|---------|
| 「开始学习」「拿下！」 | "开启您的学习之旅" |
| 「错了 3 题，AI 帮你拆」 | "智能识别您的薄弱点" |
| 「再撑 7 天」 | "距离考试还有 7 天" |

### 11.4 Code review 自检

PR diff 出现以下立即打回：

- 大块 `bg: #FFFFFF` 没改 → ❌ canvas
- `<button>` 没用 `.btn-split` 双色拼接 → ❌
- 输入框没用 `.input` 16px 字号 → ❌
- emoji 🐧 还在 → ❌ 应该用 `<img class="peng peng-XX">`
- 引入 `@mui/material` / `antd` → ❌
- 文案里出现"您 / 宝子 / 智能化" → ❌

---

## 12. Asset 目录映射

```
cert-master/
├── index.html                ← 视觉品牌手册
├── DESIGN.md                 ← 本文件（完整规范）
├── README.md                 ← 仓库使用说明
├── tokens/
│   ├── tokens.json           ← W3C Design Tokens 源数据
│   └── tokens.css            ← --cm-* CSS Variables
├── assets/
│   ├── logo/
│   │   ├── horizontal.png    ← 横版（官网 / 邮件 / 小 banner）
│   │   ├── compact.png       ← 竖版（海报 / PPT / App 启动）
│   │   ├── avatar.png        ← 圆头（头像 / 收藏 / favicon）
│   │   ├── app-icon.png      ← App Icon 通用
│   │   ├── app-icon-ios.png  ← iOS 圆角方块图标
│   │   └── avatar-icon.png   ← 96px 缩图（替代 🐧 emoji）
│   ├── mascot/               ← 8 张扁平 mascot
│   │   ├── happy.png
│   │   ├── studying.png
│   │   ├── thinking.png
│   │   ├── ai-analyzing.png
│   │   ├── sprint.png
│   │   ├── anxious.png
│   │   ├── passed.png
│   │   ├── champion.png
│   │   └── spec-sheet.png    ← 原 ChatGPT spec 图
│   ├── mascot-3d/            ← 3 张 3D 旗舰形象
│   │   ├── happy.png
│   │   ├── thinking.png
│   │   └── certified.png
│   ├── cards/                ← 4 张卡片插图
│   │   ├── wrong-book.png
│   │   ├── mock-exam.png
│   │   ├── study-plan.png
│   │   └── chapter-quiz.png
│   ├── banners/
│   │   └── hero-dark.png     ← 黑底 hero banner
│   ├── stickers/             ← 装饰贴纸（待补）
│   └── decorations/
│       └── check-sticker.png ← 3D 黄勾装饰
└── .github/workflows/
    └── deploy.yml            ← GitHub Pages 自动部署
```

---

## 13. 跟 UniMate AI 的隔离规则

Cert Master 跟 UniMate AI 同属 JR Academy，但**严格视觉/品牌隔离**：

| 维度 | UniMate AI (牛小匠) | **Cert Master (考证匠)** |
|------|---------------------|--------------------------|
| Mascot | 牛 🐂 | **企鹅 🐧** |
| Primary | Coral `#FF6B5B` | **考证黄 `#FFC52A`** |
| 主 bg | 暖白 `#FFFEF7` | **背景灰 `#F5F6F8`** |
| 主字体 | Plus Jakarta Sans | **PingFang SC** |
| 网格 | 8pt | **4pt** |
| 调性 | 学生 meme + 游戏化 | **专业 + 冷静（备考严肃）** |
| Tagline | 陪你冲 deadline | **你的 AI 考证搭子** |
| CSS 前缀 | `--um-*` | **`--cm-*`** |
| 目标用户 | 大学生 (海外华人) | **考证人 (在职 + 应届)** |

### 隔离实施

- CSS 变量前缀彻底分开（`--um-*` vs `--cm-*`），同一项目可共 import 无冲突
- Mascot 不互换：UniMate 不准出现企鹅，Cert Master 不准出现牛
- Logo / Token / Asset 各自独立 repo（unimate-ai / cert-master）

---

## 维护

- 每次改 token 必须三处同步：`tokens.json` / `tokens.css` /（如果以后加）`tokens.ts`
- 改了组件规范要在 `index.html` 同步更新视觉示例
- 改了 mascot 或 logo 必须同步更新本文件 §3 / §7 / §12
- 加新 banner 变体要同步更新 §7.2

### Sources of truth 优先级

```
DESIGN.md  ←  最高（决策源头 / 设计意图）
   ↓ 落地
tokens.json  ←  机器可读的真相（Style Dictionary / Figma Tokens）
   ↓ 翻译
tokens.css  ←  CSS Variables 实现
   ↓ 示例
index.html  ←  视觉手册 / 实景演示
```

- **冲突时**：以 DESIGN.md 为准 — 它代表"为什么这么设计"的人类意图
- **改 DESIGN.md 必须立刻同步**：tokens.json → tokens.css → index.html，缺一不可
- **token 不能擅自改**：手抖把 `#FFC52A` 写成 `#FFC52B` → 按 DESIGN.md 改回来
- **DESIGN.md 才是给设计师/PM 改的**；token 是给前端/设计工具读的

---

_v0.2 · 2026-05-11 · JR Academy_
