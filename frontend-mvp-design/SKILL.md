---
name: frontend-mvp-design
description: |
  MVP/前端 Demo 设计准备流程。触发条件：用户显式调用，或提到"mvp"、"前端demo"、"demo"。
---

# 前端设计 SOP 流程

本 skill 执行标准化的前端设计准备流程，确保设计工作有明确的图标资源和视觉参考。

## 执行步骤

### 步骤 1：选择图标库

提示用户选择前端图标库。提供以下选项：

**默认选项：**
- **Lucide** - 现代、简洁的 SVG 图标库，与 React/Vue 生态兼容性好
- **Heroicons** - Tailwind CSS 官方图标库，风格统一，有 outline/solid 两种风格
- **Ant Design Icons** - Ant Design 配套图标库，适合企业级后台系统

**用户也可以：**
- 输入自定义图标库名称
- 选择多个图标库组合使用
- 跳过（如果已有确定方案）

**提示方式：**
使用编号列表展示选项，让用户输入数字或名称选择。

---

### 步骤 2：选择 Design Prompt

提示用户选择设计 prompt 作为视觉风格参考。

**常用 Design Prompt 类别：**

| 类别 | Prompt 示例 |
|------|-------------|
| **极简主义** | Minimalist design with clean lines, generous whitespace, monochrome palette |
| **玻璃拟态** | Glassmorphism style with frosted glass effects, subtle shadows, vibrant gradients |
| **新拟态** | Neumorphism with soft shadows, extruded elements, light color scheme |
| **深色模式** | Dark mode with high contrast, accent colors, OLED-friendly deep blacks |
| **复古风格** | Retro design with vintage color palettes, serif typography, textured backgrounds |
| **赛博朋克** | Cyberpunk aesthetic with neon accents, dark backgrounds, futuristic elements |
| **自然/有机** | Organic design with natural shapes, earthy colors, flowing curves |
| **企业/商务** | Corporate design with professional blues, clean grids, authoritative typography |
| **卡片式** | Card-based layout with subtle shadows, rounded corners, clear hierarchy |
| **杂志风** | Editorial style with bold typography, asymmetric layouts, high-quality imagery |

**更多设计风格参考：**
- 访问 https://www.designprompts.dev/ 查看 31+ 种设计风格
- 用户可以直接复制该网站的 prompt
- 也可以描述自己的设计愿景，由 Claude 生成对应 prompt

**提示方式：**
1. 展示上述类别供快速选择
2. 询问是否需要查看更详细的 prompts
3. 接受用户自定义描述并转化为 design prompt

---

### 步骤 3：调用 Brainstorming

**前置检查：**
在调用 `superpowers:brainstorming` 之前，先检查该技能是否可用：
- 检查 skills 列表或尝试加载 `superpowers:brainstorming`
- 如果 `superpowers:brainstorming` 存在 → 使用该技能
- 如果 `superpowers:brainstorming` 不存在 → 改用 `frontend-design` 技能

使用可用的技能进行深入的设计探索。

**在调用前，整理已收集的信息：**
- 图标库选择
- 设计 prompt / 视觉风格方向
- 用户需求背景（如有）

**Brainstorming 时要探讨的内容：**
1. 基于 design prompt 的视觉风格具体化
2. 组件结构建议
3. 交互状态设计
4. 响应式策略
5. 技术实现要点

---

## 工作流程

```
开始
  │
  ▼
┌─────────────────────┐
│ 步骤 1: 选择图标库   │
│ • 展示默认选项       │
│ • 接受自定义输入     │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ 步骤 2: 选择 Prompt │
│ • 展示风格类别       │
│ • 接受自定义描述     │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ 步骤 3: Brainstorm  │
│ • 调用 brainstorming│
│ • 深入设计探索       │
└─────────────────────┘
```

## 输出格式

完成 SOP 后，输出一份设计准备摘要：

```markdown
## 前端设计准备摘要

### 图标库
- [已选择的图标库]

### 视觉风格参考
- [Design Prompt]

### 设计方向
- [Brainstorming 产出的关键结论]

### 下一步建议
- [具体行动项]
```

## 注意事项

- 两个选择步骤都是可选的，用户可以选择跳过
- 如果用户已有明确想法，可以快速完成 SOP
- Design prompt 应该足够具体，能指导后续设计决策
- 记录用户的选择，在后续对话中保持一致性
