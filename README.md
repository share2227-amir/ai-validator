# AI Validator — 智能交互验证官

**Intelligent Interaction Validator for AI Assistants**

A skill for AI assistants that prevents misunderstandings before they become mistakes. Activates automatically in complex analysis, decision-making, and recommendation scenarios.

[English](#english) | [中文](#中文)

---

## ✨ Features

- **Three-Layer Validation Framework** — semantic confirmation → contradiction detection → assumption surfacing
- **Proactive Clarification** — stops errors at the source, not after the fact
- **Multi-Scenario Coverage** — data analysis, business advice, logical reasoning, content generation
- **Quick Commands** — `/validate`, `/check`, `/challenge`, `/assumptions`

---

## 📦 Installation

### Via SkillHub (Recommended)

```
skillhub install ai-validator
```

### Manual Install

1. Download this repository
2. Place the `ai-validator` folder into your skills directory:
   - **QClaw / OpenClaw**: `~/.qclaw/skills/`
   - **Claude Code**: `~/.claude/skills/`
3. Restart your AI assistant

---

## 🚀 Quick Start

### Automatic Trigger

The skill activates automatically when:
- User provides data for analysis
- User describes a business scenario requesting advice
- User asks to "verify", "validate", or "confirm understanding"
- Task involves data scope, time range, or definition boundaries

### Manual Commands

| Command | Description |
|---------|-------------|
| `/validate` | Full three-layer validation of current conversation |
| `/check` | Quick semantic confirmation (Layer 1) |
| `/challenge` | Activate critical scrutiny mode (Layer 2) |
| `/assumptions` | List hidden assumptions (Layer 3) |

---

## 🏗️ Three-Layer Validation Framework

### Layer 1 — Semantic Understanding & Feedback

Restate your core request in the AI's own words before execution begins.

```
You: Analyze our Q1 cumulative sales data.

AI: I understand you'd like me to analyze Q1 cumulative sales.
Before I proceed, I need to confirm:
- Does "cumulative" mean year-to-date totals per month?
- What dimensions should I analyze — trends, YoY comparison, or structure?
```

### Layer 2 — Contradiction Detection & Critical Questions

Scan for logical inconsistencies in your input:

- Internal consistency (do the facts align with each other?)
- External factual consistency (does it conflict with known facts?)
- Time/logic sequence (is the chronology reasonable?)

### Layer 3 — Assumption Surfacing & Risk Assessment

Before generating results, explicitly list hidden assumptions and ask for confirmation:

```
AI: To build the budget, I need to work with these assumptions:
1. Market conditions and competitor strategy remain stable
2. Sales channels and team capacity stay constant

If these don't hold, the plan needs adjustment.
Do you confirm these assumptions, or should I account for changes?
```

---

## 📋 Protocol Flow

```
1. Receive Input → Get user's instruction and context

2. Layer 1: Understanding → Summarize, ask for confirmation

3. User Confirms/Corrects → If corrected, return to Step 2

4. Layer 2: Contradiction Scan → Check logical & factual consistency

5. Find Issues → Ask specific, actionable clarification questions

6. User Clarifies → Get clarified information

7. Layer 3: Assumptions & Risks → List hidden assumptions, get final authorization

8. Execute → Only now perform the actual work
```

---

## 📝 License

MIT License — free to use, modify, and distribute.

---

*AI Validator v1.0.0 — Prevention is better than correction.*
