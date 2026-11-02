---
name: flat-ui-design-system
description: 做图表、流程图、UI mockup、仪表盘、交互说明页或任何嵌在对话/网页里的视觉组件时用：强制扁平、暗亮双模式、CSS 变量、复杂度上限，避免花哨渐变与大段说明塞进组件。
---

# flat-ui-design-system

来源学习笔记（非官方授权）：对标公开流传的 Claude 视觉组件设计约束（模块选型 + Core Design System）。用于 Grok Bot / 自媒体相关 bot 出图、出 HTML 排版卡、仪表盘样张。

## 何时启用
- 画 diagram / mockup / chart / interactive / art 任一视觉
- 写公众号/图文 HTML 卡片、封面旁的信息卡、数据面板
- Canvas / 小工具 UI

## 先选模块
选最接近的一类，并只加载该类约束：
- **diagram**：SVG 流程图、结构图、示意
- **mockup**：界面线框、表单、卡片、仪表盘
- **interactive**：可控件交互的说明页
- **chart**：图表、数据分析、地图（Chart.js / D3 等）
- **art**：插画与生成艺术

## 复杂度硬上限
1. 盒子副标题 ≤5 个英文词或 ≤8 个汉字；细节放点击展开或正文，不塞进盒子。
2. 一张图颜色渐变轴 ≤2；颜色表意必须加一行图例，否则只用中性色。
3. 全宽横排盒子 ≤4（约 140px 宽）；≥5 个则缩到 ≤110px、折两行，或拆成「总览 + 细节」两张图。

## 哲学（全局）
- **Seamless**：组件看起来像宿主产品原生，不要另起一套皮肤。
- **Flat**：禁止渐变、mesh、噪点、装饰特效。
- **Compact**：组件里只放必要信息；解释写在聊天/正文。
- **文视分离**：说明、引言、总结写在回复正文；组件输出只放视觉本身。禁止把大段 prose、章节标题塞进 HTML/SVG。

## 流式输出顺序
短 `<style>` → 内容 HTML → `<script>` 放最后，让有用内容尽早出现。

## CSS 变量（必须用变量，禁硬编码色）
### Surfaces
- `--surface-0` 页面底
- `--surface-1` 卡片下一级
- `--surface-2` 主卡片（偏白/亮面）
- 角色底：`--bg-{accent,danger,success,warning}`

### Text
- `--text-primary` / `--text-secondary` / `--text-muted`
- 角色字：`--text-{accent,danger,success,warning}`

### Borders
- `--border` 默认发丝线
- `--border-strong` / `--border-stronger`
- 角色边：`--border-{accent,danger,success,warning}`

### Type & layout
- 字体：`--font-sans`、`--font-voice`（衬线）、`--font-mono`
- `--radius` 默认 8px；更大圆角用字面量 12px/16px
- 间距：`--pad-{sm,md,lg,xl}`、`--gap-{xs,sm,md,lg,xl}`

## 暗色模式
每个颜色必须在亮/暗下都可读。SVG 用预置色类（如 `c-blue`/`c-teal`/`c-amber`）；禁止为颜色单独写 `<style>`；每个 `<text>` 必须有类（`t`/`ts`/`th`）；禁止省略 fill 或 `fill="inherit"`。

## Mockup / 组件细则
- 容器宽约 **680px**；栅格用 `repeat(auto-fit, minmax(160px, 1fr))`。
- 美学：扁平、干净亮面、0.5px 边、留白充足；无渐变、无阴影（焦点环除外）。
- 边框：`0.5px solid var(--border)`（强调用 `--border-strong`）。
- 卡片：`var(--surface-2)` + 0.5px 边 + 12px 圆角 + `padding: 1rem 1.25rem`。
- 表单控件用原生标签即可（input/select/textarea/button/range）；文本框高约 36px；range 轨道 4px、拇指 18px。
- 需要「再想一步」的动作，用明确的交互回调（如 `sendPrompt()` 一类），不要塞说明段落进组件。

## 自检清单（交付前）
- [ ] 模块选对
- [ ] 未超复杂度上限
- [ ] 无渐变/阴影装饰
- [ ] 颜色全走变量且双模式可读
- [ ] 解释在正文，组件里无长文
- [ ] 卡片边与圆角符合规范

## 不适用
- 真人摄影封面、品牌插画自由发挥（走 art/封面规范另开）
- 需要强营销视觉冲击的短视频封面（另用对应封面技能）
