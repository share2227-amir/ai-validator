# AI Validator · 智能交互验证官

**An AI skill that catches misunderstandings before they become mistakes.**

Supports Chinese and English. See below for English documentation.

---

## 🇨🇳 中文说明

### 这是什么

AI Validator 是一个 AI 助手技能插件，在执行复杂分析、决策建议、数据处理等关键任务前，自动对用户的指令进行三层验证：语义确认 → 矛盾检测 → 假设显性化。

### 核心价值

**准确性优于响应速度。** 允许多花一轮对话来确保理解正确，好过做完才发现方向错了。

### 安装方式

**方式一（推荐）：SkillHub**
```
skillhub install ai-validator
```

**方式二：手动安装**
1. 下载本仓库
2. 将 `ai-validator` 文件夹放入你的 skills 目录：
   - QClaw / OpenClaw：`~/.qclaw/skills/`
   - Claude Code：`~/.claude/skills/`
3. 重启 AI 助手

### 快速指令

| 指令 | 说明 |
|------|------|
| `/validate` | 对当前对话执行完整三层验证 |
| `/check` | 快速语义理解确认（第一层） |
| `/challenge` | 激活批判性质疑模式（第二层） |
| `/assumptions` | 列出当前任务的隐含假设（第三层） |

### 三层验证框架

**第一层：语义理解与即时反馈**
在执行任何指令前，用自己的话复述用户的核心请求，确保理解一致。

```
用户：请分析这组季度数据。

AI：我理解您希望分析这组季度数据。
在开始之前，我需要确认：
- 这组数据是2026年第一季度的累计值还是单季度值？
- 您希望从哪个维度分析——趋势、同比、还是结构占比？
```

**第二层：矛盾检测与批判性提问**
扫描用户输入中的逻辑矛盾、事实不一致、时间序列问题。

发现矛盾时，以建设性口吻发起澄清提问，不对抗、不指责。

**第三层：假设显性化与风险评估**
在生成结论前，主动列出为完成任务所做的隐含假设，并征询用户确认。

```
AI：在制定预算前，我需要基于以下假设：
1. 市场环境无重大突发变化
2. 销售渠道和团队效能保持稳定
如果这些假设不成立，方案需要调整。
您是否同意在这些假设下继续？
```

### 交互流程

```
1. 接收输入
2. 第一层：理解反馈 → 输出摘要，等待确认
3. 用户确认/修正 → 若修正，回到步骤2
4. 第二层：矛盾扫描 → 检查逻辑与事实一致性
5. 发现问题 → 提出具体可操作的澄清问题
6. 用户澄清
7. 第三层：假设与风险 → 列举隐含假设，获取最终授权
8. 执行与输出
```

### 使用场景

| 场景 | 验证重点 | 典型问题 |
|------|---------|---------|
| 数据分析 | 数据口径、时间范围、单位 | "这是累计值还是当期值？" |
| 业务建议 | 前提假设、约束条件 | "我假设预算上限是X，对吗？" |
| 逻辑推理 | 前提真实性、推理链条 | "这个结论依赖的前提是..." |
| 内容生成 | 受众定位、风格要求 | "目标读者是谁？需要什么语气？" |

---

## 🇺🇸 English

### What Is This

AI Validator is an AI assistant skill that activates before complex tasks — analysis, decisions, data processing — to ensure understanding is correct through a three-layer validation: semantic confirmation → contradiction detection → assumption surfacing.

### Core Value

**Accuracy over speed.** Spend an extra round of conversation to confirm understanding, rather than discover the direction was wrong after the work is done.

### Installation

**Option 1 (Recommended) — SkillHub**
```
skillhub install ai-validator
```

**Option 2 — Manual Install**
1. Download this repository
2. Place the `ai-validator` folder into your skills directory:
   - QClaw / OpenClaw: `~/.qclaw/skills/`
   - Claude Code: `~/.claude/skills/`
3. Restart your AI assistant

### Quick Commands

| Command | Description |
|---------|-------------|
| `/validate` | Full three-layer validation of current conversation |
| `/check` | Quick semantic confirmation (Layer 1) |
| `/challenge` | Activate critical scrutiny mode (Layer 2) |
| `/assumptions` | List hidden assumptions (Layer 3) |

### Three-Layer Framework

**Layer 1 — Semantic Understanding & Feedback**
Before execution, restate the user's core request in your own words.

**Layer 2 — Contradiction Detection & Critical Questions**
Scan for logical inconsistencies: internal conflicts, factual misalignment, unreasonable time sequences.

**Layer 3 — Assumption Surfacing & Risk Assessment**
Before generating results, explicitly list all hidden assumptions and request confirmation.

### License

MIT License — free to use, modify, and distribute.

---

*AI Validator v1.0.0 — Prevention is better than correction.*
