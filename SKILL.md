# Paper Revision (sci-writestructure)

## I. Purpose and Trigger

### 1.1 What this skill does

Diagnoses and revises existing manuscript drafts section by section based on the IMRAD skeleton and universal SCI writing standards. The knowledge base consists of four reference files with complementary roles:

| Reference file | Role | Provides |
|----------------|------|----------|
| `references/paper-criteria.md` | Principles | "Should it be written this way?" — Starting原创性自检 (4 questions) + IMRAD principles per section |
| `references/sci-writing-standard.md` | Recipes | "How to write it specifically" — word counts, sentence formulae, skeleton templates, pitfalls per section |
| `references/phrase-bank.md` | Phrases | "Which sentences to use" — English sentence skeletons organised by section (Part A) and by function (Part B) |
| `references/discipline-templates.md` | Disciplines | M&M and metric phrasing for non-life-science disciplines (STEM/CS, Econ, Humanities/Social Sciences) |

Language-agnostic: works for both Chinese and English drafts.

### 1.2 When to activate

- User uploads or pastes a manuscript draft requesting revision, polishing, or structural review.
- User asks about a specific section (e.g., "How is my Introduction?", "What type of abstract should I use?", "Is my figure legend self-sufficient?").
- User explicitly invokes this skill or says "follow the framework to revise", "use the paper-revision standard to review my draft".

---

## II. Workflow

### Step 0 — Intake

Confirm the following with the user (do not fabricate manuscript content if information is missing):

1. **Manuscript location**: file path or pasted text. For `.docx` / `.pdf` / `.tex` binaries, extract plain text and figure/table list first via a document parser; **do not guess unextracted content**.
2. **Review scope**: infer from user input — if specific sections are named (e.g., "review Introduction and Discussion"), review only those; otherwise default to full-paper review.
3. **Discipline**: infer from manuscript content; default to life sciences/agriculture (use `phrase-bank.md`) if unidentifiable. If clearly non-life-science (STEM/CS, Econ, Humanities/Social Sciences), load `references/discipline-templates.md` (D1–D5) for discipline-specific M&M and metric phrasing. Generic functional phrases (gap, method choice, result statement, conclusion, references) remain cross-disciplinary — still from `phrase-bank.md` Part B.

### Step 1 — Starting原创性自检 (Gate)

Evaluate each of the four questions per `references/paper-criteria.md` Section 一:

1. Have you done something new and interesting?
2. Is there anything challenging in your work?
3. Is the work directly related to a current hot topic?
4. Have you provided solutions to any difficult problems?

Give a **yes/no** verdict with a one-sentence reason for each. This is a **non-blocking pre-check**: if any item is no, flag the risk at the top of the report (e.g., "Core novelty unclear — recommend clarifying contribution before heavy polishing"), but do not block structural revision.

> Semantic note: the source framework treats "all 4 yes" as a prerequisite for beginning writing; this skill is for revising **existing manuscripts**, so it is implemented as a non-blocking pre-check — the difference is explicit to avoid confusion.

### Step 2 — Section-by-Section Structured Review

Review all 10 sections in natural paper order (see `sci-writing-standard.md` Section 0). Per section:

1. **Load standards**: load the detailed recipe for the corresponding anchor point in `references/sci-writing-standard.md` as the primary standard; also consult the matching `#` anchor in `references/paper-criteria.md`. For non-life-science manuscripts, additionally load `references/discipline-templates.md` for the relevant discipline (D1–D5).
2. **Cross-check line by line** against the draft; flag violations or weaknesses.
3. **Record each issue** with four fields:
   - **Location** (section + quoted text fragment)
   - **Violated standard** (reference to framework item)
   - **Severity** (High / Medium / Low)
   - **Specific revision suggestion**: retrieve an English sentence skeleton from `references/phrase-bank.md` appropriate for the section/function, replace `XXX`/`X`/`Y` placeholders with the author's actual variables, and present a **ready-to-use sentence** — never a vague suggestion. Never copy a template example sentence verbatim (see execution rule "禁止逐字照搬").

**Severity decision tree** (evaluate top-down, stop at first match):

> Start from the most severe condition and check downwards — if an issue matches both "High" and "Medium", record it as High and note the Medium-level impact in the suggestion.

1. **Data/conclusion errors, missing core elements (e.g., abstract without results / introduction without gap), reproducibility/ethics violations, figure-text contradictions?** → **High** — directly threatens credibility or acceptability, must be fixed.
2. **Incomplete argument chain (gap not specific, results not mirroring methods), structural confusion (Results/ Discussion bleed), wrong abstract type/word count, non-standard keywords?** → **Medium** — weakens persuasiveness but not fatal.
3. **Everything else?** → **Low** — phrasing quirks, wordiness, minor reference format issues; does not affect scientific content.

**Figure/table boundary**: visual elements (error bars, N values, figure-text consistency) cannot be verified from plain text. Flag such items as "needs visual verification" without asserting pass/fail.

**Section-to-anchor mapping**:

| Section | Primary anchor | Principles anchor | Key review points |
|---------|---------------|-------------------|-------------------|
| Title | `## 1. Title` | `#2.1` | 15–22 words; object + method + highlight; avoid (questions, abbreviations, exaggeration) |
| Abstract | `## 2. Abstract` | `#2.2` | 5-part, 200–250 words; pain→gap→method→data→significance; no references |
| Keywords | `## Keywords` | `#2.3` | Matches author guidelines; reflects substantive topic; no non-standard abbreviations |
| Introduction | `## 3. Introduction` | `#2.4` | Background→status→gap→purpose→significance; gap must be specific and addressable by this paper |
| Methods | `## 4. Materials and Methods` | `#2.5` | Reproducible; materials traceable; statistical methods explicit |
| Results | `## 5. Results` | `#2.6` | Data only, no interpretation; figures/tables self-sufficient with complete annotations |
| Discussion | `## 6. Discussion` | `#2.7` | 4-step method; benchmark literature; deep mechanism; acknowledge limitations |
| Conclusion | `## 7. Conclusion` | `#2.8` | 3-sentence template; do not repeat Discussion; no new data/conclusions |
| Acknowledgments | — | `#2.10` | Fund sources, ethics approval/informed consent, COI statement; no omissions, no unauthorized acknowledgements |
| References | — | `#2.9` | Matches journal style; ≥70% highly cited within 3–5 years; cite journal's own papers; no incorrect DOIs |

> **M&M templates vary by discipline**: life sciences/medicine see `phrase-bank.md` A4; STEM/CS/engineering, economics, agriculture, humanities/social sciences see `discipline-templates.md` D1–D4 (discipline-to-template routing table at the end of that file). Generic functional phrases remain in `phrase-bank.md` Part B.

### Step 3 — Produce Review Report (default deliverable)

Structured Markdown report:

- **Top**: originality self-check results + overall evaluation (strengths / top issues).
- **Section-by-section table**: `| ID | Section | Issue | Severity | Standard | Suggestion |` (IDs use `R1`, `R2`… format for Step 4 referencing). Suggestions should be **ready-to-use sentences with the author's variables substituted** (borrow only the skeleton from `phrase-bank.md`; never copy template example sentences verbatim).
- **Bottom**: revised issue list ordered by severity (high first).

**Report skeleton** (consistent across uses):

```
# Manuscript Review Report
## 0. Originality Self-Check (4 questions)
| Question | Verdict | Reason |
|----------|---------|--------|
| ① New and interesting | yes/no | ... |
| ② Challenging | yes/no | ... |
| ③ Related to hot topic | yes/no | ... |
| ④ Provides solution | yes/no | ... |
Overall: strengths / top issues

## 1. Section-by-Section Review
| ID | Section | Issue | Severity | Standard | Suggestion |
|----|---------|-------|----------|----------|------------|
| R1 | ... | ... | H/M/L | sci-writing-standard `## x` / paper-criteria `#2.x` | Phrase from phrase-bank `A#/B#` |

## 2. Revision Checklist (ordered by severity, with R# IDs)
- R1. [High] ...
- R2. [Medium] ...
- R3. [Low] ...
```

Report must be self-contained and readable without prior conversation context.

### Step 4 — Apply Edits (opt-in)

After delivering the report, **ask the user** whether to apply suggestions to the manuscript:

- **A All edits** (default) → AI revises per report item by item.
- **B Selective edits** → user specifies IDs, sections, or severity (e.g., "fix R1 and R3", "only Discussion", "fix High and Medium").
- **C No edits** → user handles manually; flow ends.
- **Application method**: modify the original file (keeping change traceability) or produce a "revised version" file + **change log** (listing each `R#` → actual change) for easy rollback.
- **Never modify the user's file without explicit confirmation.**

### Step 5 — Re-review (opt-in)

After edits are applied, **ask the user** whether a re-review is needed. Confirm to verify corrected items; skip to end if declined.

---

## III. Execution Rules

### 3.1 Context-loading strategy

**Do not load any reference file into context wholesale.** Load on demand only:

1. **Step 1 Originality check** → `grep -A 15 "一、Starting" references/paper-criteria.md`
2. **Step 2 Section review (per section independently)**:
   - Primary standard (replace `N` with section number, e.g., `## 1.`, `## 2.`): `grep -A 20 "^## N\\." references/sci-writing-standard.md`
   - Principles reference (replace `N` with section number, e.g., `2.1`, `2.2`): `grep -A 15 "^### 2\\.[0-9]" references/paper-criteria.md`
   - Non-life-science manuscripts additionally: `grep -A 10 "^## D[1-5]" references/discipline-templates.md`
3. **Revision suggestions (during Step 2 issue recording)**:
   - By section (A1–A8, replace `N` with digit): `grep -A 10 "^### A[1-8]" references/phrase-bank.md`
   - By function (B1–B13, replace `N` with digit): `grep -A 10 "^### B[0-9]" references/phrase-bank.md` and `grep -A 10 "^### B[0-9][0-9]" references/phrase-bank.md` (for B10–B13)
4. **After reviewing each section, actively release that section's context** before switching to the next.

### 3.2 Issue data structure

Each issue recorded in Step 2 must strictly follow this structure. Step 3 reporting and Step 4 selective application both depend on its completeness:

```
Each issue = {
  id:       "R1"           // auto-incrementing, for Step 4 referencing
  section:  "Discussion"   // which section
  problem:  "未对标前人文献，第3段结论缺少文献支撑"  // issue description (with quoted text)
  severity: "Medium"       // High / Medium / Low — per Step 2 decision tree
  ref:      "sci-writing-standard ## 6.2"  // violated standard
  suggestion: "建议补充：'Our findings are consistent with those reported by Smith et al. (2020), who found that…'"  // ready-to-use suggestion
}
```

Record each issue as a separate fenced code block or list entry to preserve all fields during Step 3 formatting.

### 3.3 Quality criteria

- **Evidence first**: every issue must cite a manuscript excerpt; no guessing.
- **Specific suggestions**: provide usable sentences, not "suggest making it clearer".
- **Phrases grounded**: English revision suggestions优先 from `phrase-bank.md` sentence **skeletons**; when套用, variables must come from the author's manuscript. Self-authored sentences only when clearly necessary, and mark them as such.
- **Distinguish fact from opinion**: framework standards are factual; "is it novel" is judgment — label it as such.
- **Language matching**: Chinese draft → Chinese review terminology; English draft → English terminology; standards themselves are bilingual.
- **Respect the original**: revision optimises expression and structure; never alter the author's scientific conclusions or data.
- **No verbatim template copying**: only borrow structure and function from `phrase-bank.md`; **variables must come from the author's manuscript**; output sentences should vary — avoid every manuscript starting the same way; for template examples with specific content (e.g., `because of the rarity of this cancer`), replace with the author's actual research subject. **Purpose**: templates are structural guides only, ensuring original expression and preventing unintentional copying.