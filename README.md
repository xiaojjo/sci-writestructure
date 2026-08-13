# Paper Revision (sci-writestructure)

> Diagnose and revise academic manuscript drafts section by section — based on IMRAD structure and universal SCI writing standards.

---

## Overview

`sci-writestructure` is a Hermes Agent skill that reviews SCI manuscript drafts against a structured checklist, then produces a severity-ranked revision report with ready-to-use sentence suggestions.

**What it does:**

- Runs a 4-question originality gate before detailed review
- Checks all 10 paper sections (Title → References) against journal-grade standards
- Produces a Markdown review report with ranked issues and actionable suggestions
- Applies edits only after user confirmation

**What it covers:**

STEM / Humanities / Medicine / Agriculture / Economics — language-agnostic, works for both Chinese and English drafts.

---

## Workflow

```mermaid
flowchart TB
    %% 定义样式（强制黑色文字）
    classDef startEnd fill:#e1f5fe,stroke:#01579b,stroke-width:2px,color:#000000;
    classDef process fill:#f3e5f5,stroke:#4a148c,stroke-width:2px,color:#000000;
    classDef decision fill:#fff3e0,stroke:#e65100,stroke-width:2px,color:#000000;
    classDef risk fill:#ffebee,stroke:#c62828,stroke-width:2px,color:#000000;

    A[提交稿件] --> B[步骤0：收稿登记]
    B --> C[步骤1：原创性初审<br>（4项预检）]
    C --> D{预检结果中<br>是否有“否”？}
    
    D -->|是（存在风险项）| E[打上风险标记]
    D -->|否（全部通过）| F[步骤2：栏目复审]
    E --> F
    
    F --> G[步骤3：生成审稿报告]
    G --> H{是否需要<br>应用编辑修改？}
    
    H -->|是| I[步骤4：执行修改]
    H -->|否| J[流程结束]
    
    I --> K{是否需要<br>重新复审？}
    K -->|是| F
    K -->|否| J

    %% 应用样式
    class A,B startEnd;
    class C,F,G,I process;
    class D,H,K decision;
    class E risk;
    class J startEnd;
```

**Step summary**

| Step | Action | Deliverable |
|------|--------|-------------|
| 0 — Intake | Confirm manuscript, scope, discipline | — |
| 1 — Originality Gate | 4-question pre-check (non-blocking) | Risk flag if any no |
| 2 — Section Review | Load standards per section; cross-check draft | Issue list with severity + suggestion |
| 3 — Report | Generate structured Markdown report | `# Manuscript Review Report` |
| 4 — Apply Edits | Modify original or produce revised version | Change log (R# → actual change) |
| 5 — Re-review (opt-in) | Verify corrections | Updated report or end |

---

## Quick Start

**In Hermes Agent:**

```
@sci-writestructure  review my manuscript at D:/path/to/draft.docx
```

Or paste text directly:

```
@sci-writestructure  here is my Discussion section — please review
```

The agent will automatically trigger the full workflow.

---

## File Structure

```
SKILL.md                       ← Main workflow + execution rules
references/
  paper-criteria.md            ← Originality gate + per-section principles
  sci-writing-standard.md      ← Per-section recipes (word counts, pitfalls)
  phrase-bank.md               ← English sentence skeletons by section & function
  discipline-templates.md      ← Non-life-science M&M and metric phrasing
```

---

## Key Design Decisions

- **Non-blocking gate**: originality check flags risk but never blocks revision
- **On-demand loading**: reference files are `grep`-loaded per section; never loaded wholesale
- **Severity-driven**: High → Medium → Low; each issue gets a ready-to-use sentence suggestion
- **No verbatim template copying**: variables always come from the author's manuscript
- **Opt-in edits**: never modify the user's file without explicit confirmation

---

## License

MIT — use, modify, and distribute freely.
