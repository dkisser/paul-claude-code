---
name: frontend-mvp-design
description: |
  MVP/前端 Demo 设计准备流程。触发条件：用户显式调用，或提到"mvp"、"前端demo"、"demo"。
---

# 前端设计 SOP 流程

本 skill 执行标准化的前端设计准备流程，确保设计工作有明确的图标资源和视觉参考。

**重要：本流程必须一步一步执行，每步都需要等待用户明确回复后再进入下一步。**

## 执行流程概览

整个 SOP 流程包含 3 个步骤，必须按顺序执行：

1. **步骤 1**：选择图标库（必须获得用户明确选择后才能进入下一步）
2. **步骤 2**：选择 Design Prompt（必须获得用户明确选择后才能进入下一步）
3. **步骤 3**：调用 Brainstorming 进行深入设计探索

---

## 步骤 1：选择图标库

**指令：必须先完成此步骤并获得用户明确回复，才能继续步骤 2。**

向用户展示以下图标库选项，并等待用户做出选择：

**请选择图标库（输入数字或名称）：**

1. **Lucide** - 现代、简洁的 SVG 图标库，与 React/Vue 生态兼容性好
2. **Heroicons** - Tailwind CSS 官方图标库，风格统一，有 outline/solid 两种风格
3. **Ant Design Icons** - Ant Design 配套图标库，适合企业级后台系统
4. **其他** - 请告诉我你想使用的图标库名称
5. **跳过** - 已有确定的图标库方案

**等待用户回复后：**
- 记录用户选择的图标库
- 确认用户选择（例如："好的，您选择了 Lucide 图标库。"）
- **明确询问**："现在进入步骤 2：选择视觉风格 Design Prompt，您准备好了吗？"
- **只有在用户明确同意后，才进入步骤 2**

---

## 步骤 2：选择 Design Prompt

**指令：必须先完成此步骤并获得用户明确回复，才能继续步骤 3。**

向用户展示以下设计风格选项，并等待用户做出选择：

**请选择视觉风格（输入数字或描述您的想法）：**

| 编号 | 类别 | Prompt 示例 |
|------|------|-------------|
| 1 | **极简主义** | Minimalist design with clean lines, generous whitespace, monochrome palette |
| 2 | **玻璃拟态** | Glassmorphism style with frosted glass effects, subtle shadows, vibrant gradients |
| 3 | **新拟态** | Neumorphism with soft shadows, extruded elements, light color scheme |
| 4 | **深色模式** | Dark mode with high contrast, accent colors, OLED-friendly deep blacks |
| 5 | **复古风格** | Retro design with vintage color palettes, serif typography, textured backgrounds |
| 6 | **赛博朋克** | Cyberpunk aesthetic with neon accents, dark backgrounds, futuristic elements |
| 7 | **自然/有机** | Organic design with natural shapes, earthy colors, flowing curves |
| 8 | **企业/商务** | Corporate design with professional blues, clean grids, authoritative typography |
| 9 | **卡片式** | Card-based layout with subtle shadows, rounded corners, clear hierarchy |
| 10 | **杂志风** | Editorial style with bold typography, asymmetric layouts, high-quality imagery |
| 11 | **自定义** | 描述您的设计愿景，我来生成对应 prompt |

**附加选项：**
- 输入 "more" 查看更多设计风格参考
- 访问 https://www.designprompts.dev/ 查看 31+ 种设计风格

**等待用户回复后：**
- 记录用户选择的视觉风格
- 确认用户选择（例如："好的，您选择了极简主义风格。"）
- 整理已收集的信息：图标库选择 + 设计 prompt
- **明确询问**："现在进入步骤 3：进行深入的设计探索（Brainstorming），您准备好了吗？"
- **只有在用户明确同意后，才进入步骤 3**

---

## 步骤 3：调用 Brainstorming

**前置检查：**
在调用 `superpowers:brainstorming` 之前，先检查该技能是否可用：
- 检查 skills 列表或尝试加载 `superpowers:brainstorming`
- 如果 `superpowers:brainstorming` 存在 → 使用该技能
- 如果 `superpowers:brainstorming` 不存在 → 改用 `frontend-design` 技能

**调用前准备：**
整理已收集的所有信息：
- 图标库选择：[步骤 1 的结果]
- 设计 prompt / 视觉风格方向：[步骤 2 的结果]
- 用户需求背景（如有）

**Brainstorming 时要探讨的内容：**
1. 基于 design prompt 的视觉风格具体化
2. 组件结构建议
3. 交互状态设计
4. 响应式策略
5. 技术实现要点

**完成后：**
输出设计准备摘要（见下文输出格式）

---

## 工作流程图示

```
开始
  │
  ▼
┌─────────────────────────┐
│ 步骤 1: 选择图标库       │
│ • 展示选项               │
│ • 等待用户选择           │
│ • 获得明确回复 ✓         │
└───────────┬─────────────┘
            │ 用户确认后
            ▼
┌─────────────────────────┐
│ 步骤 2: 选择 Prompt     │
│ • 展示风格类别           │
│ • 等待用户选择           │
│ • 获得明确回复 ✓         │
└───────────┬─────────────┘
            │ 用户确认后
            ▼
┌─────────────────────────┐
│ 步骤 3: Brainstorm      │
│ • 调用 brainstorming    │
│ • 深入设计探索           │
└─────────────────────────┘
```

---

## 输出格式

完成所有 3 个步骤后，输出一份设计准备摘要：

```markdown
## 前端设计准备摘要

### 图标库
- [步骤 1 中用户选择的图标库]

### 视觉风格参考
- [步骤 2 中用户选择的 Design Prompt]

### 设计方向
- [Brainstorming 产出的关键结论]

### 下一步建议
- [具体行动项]
```

---

## 注意事项

1. **严格分步执行**：每个步骤必须等待用户明确回复后才能进入下一步
2. **确认机制**：每完成一个步骤后，明确告知用户已完成并询问是否进入下一步
3. **用户控制**：用户可以随时选择跳过某一步骤或修改之前的选择
4. **记录选择**：记录用户在每一步的选择，在后续对话中保持一致性
5. **灵活处理**：如果用户在一次回复中提供了多个步骤的信息，可以灵活调整但仍需确认每个选择
