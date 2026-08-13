# Paper Revision Criteria

This file is the knowledge base for the `sci-writestructure` skill, containing the full "Starting原创性自检 + article architecture" writing standards. During review, load only the relevant section anchors (`#2.1`–`#2.10`) on demand to avoid context overflow. The standards are language-agnostic and apply to both Chinese and English drafts.

---

## 一、Starting原创性自检 (Pre-writing Gate)

> Before drafting or revising, confirm whether the study is worth writing up as a paper (originality pre-check). This skill is for **revising existing manuscripts**, so this is a **non-blocking pre-check**: all four yes = strong originality; any no = flag risk at report top, but do not block structural revision (consistent with SKILL.md Step 1).

Evaluate each of the following four questions:

1. **Have you done something new and interesting?**
2. **Is there anything challenging in your work?**
3. **Is the work directly related to a current hot topic?**
4. **Have you provided solutions to any difficult problems?**

**Verdict rule**: all four yes → proceed to revise. Any no → flag risk (e.g., "Core novelty unclear — clarify contribution before heavy polishing"), but structural revision is not blocked.

---

## 二、Article Architecture

### 2.1 Title

A good title: **describe the paper's substance with as few words as possible**.

Characteristics of effective titles:

- Identify the main issue of the paper.
- Begin with the subject of the paper.
- Are accurate, unambiguous, specific, and complete.
- Do not contain infrequently-used abbreviations.
- Attract readers.

**Review points**: Is the title too broad or too narrow? Does it contain unfamiliar abbreviations? Can the research object and core finding be seen at a glance?

---

### 2.2 Abstract

Three main types of abstract (source: ICELE 2008):

- **Indicative (descriptive) abstract**: outlines the topic; helps readers decide whether to read further; common for reviews or conference reports.
- **Informative abstract**: summarises the paper following IMRAD structure without explicit subheadings.
- **Structured abstract**: follows journal-required subheadings (often Background/Methods/Results/Conclusion); common in medical journals.

> **Must do**: confirm the target journal's required abstract type before reviewing.

An abstract is "the advertisement of your article" and must be:

- Precise and honest.
- Self-sufficient (readable without the full text).
- Free of technical jargon.
- Brief and specific.
- Free of reference citations.

**Review points**: Does the abstract type match the journal? Can it stand alone? Are there reference numbers? Overuse of domain-specific jargon?

---

### 2.3 Keywords

Used for indexing.

- Check the Guide for Authors for quantity, numbering, definition, subject heading list, and other special requirements.
- Selected words should reflect the essential topics of the article; avoid overly broad words like "market" or "method".
- Only use abbreviations firmly and unambiguously established in the field.

**Review points**: Do quantity/format match the journal's author guidelines? Are terms too broad? Are non-standard abbreviations included?

---

### 2.4 Introduction

Answer a series of questions:

- What is the problem?
- Are there any existing solutions?
- Which is the best?
- What is its main limitation?
- What do you hope to achieve?

**Background information**: provide sufficient context so readers can evaluate your work (`general background (review of cited literature) → the specific problem this study addresses`).

**Persuade the reader of necessity**: use *however*, *remain unclear*, etc. to introduce your opinion and research gap.

**Notes**:

- If you want to present new data, first place it in perspective.
- Be concise — this is not a history lecture.
- Do not confuse Introduction, Results, Discussion, and Conclusion — keep them separate.
- Do not overuse *novel*, *first time*, *first ever*.

**Review points**: Have all five questions been answered? Is the research gap clear? Are Results/Discussion content sneaking in? Is "first/novel" overused?

---

### 2.5 Methods

**How did you study the problem?**

Basic principle: provide sufficient information so an informed reader can reproduce the experiment or derivation.

- **Empirical papers**: material studied, area descriptions; methods, techniques, theories applied.
- **Case study papers**: application of existing methods/theories/tools; special settings of this study.
- **Methodology papers**: materials and detailed procedure of a novel experimentation; scheme, flow, and performance analysis of a new algorithm.

**Analytical techniques?**

- Describe analytical methods if not universally understood.
- Why was this method chosen?
- What are the method's data requirements?
- What are the major concerns when using this technique?
- Cite justification for selection of the method if necessary.

**Review points**: Is it at a reproducibility level? Are the contents appropriate for the paper type (empirical/case/methodology)? Is method selection justified?

---

### 2.6 Results

**What should be included**:

- Main findings listed in association with the methods.
- Highlighted difference between your results and previous publications (especially case studies).
- Results of statistical analysis.
- Results of performance analysis (especially for methodology or algorithm papers).
- A set of principle equations or theorems supporting the assumptions (especially for theory papers).

**Make captions self-sufficient**: figure/table titles should contain sufficient information for the figure to be understood without the main text.

**Notes**:

1. Illustrations should not duplicate information described elsewhere.
2. Do not use confusing figures.
3. Appearances count:
   - Draw 3 or 4 datasets per figure;
   - Use subpanels to assemble figures illustrating the same class of problem;
   - Select appropriate scales; proper axis label sizes; symbols clearly visible; datasets easy to distinguish.

**Review points**: Do results mirror the methods? Is statistical/performance analysis provided? Are figure captions self-sufficient? Is there figure-text duplication or overly fancy figures?

---

### 2.7 Discussion

**Check the following**:

- How do your results relate to the research questions/objectives outlined in the Introduction?
- Can a smooth conclusion follow from the discussion?
- Is an explanation provided for each result presented?
- Are your results consistent with or different from other researchers'? Why?
- Are there any limitations?

**Do not**:

- Make statements that go beyond what the results can support.
- Suddenly introduce new terms or ideas.

**Quantitative description is always preferred**:

- Poor: *There was a significant relationship between last year's satisfaction score and this year's profit margins.*
- Better: *There was a 0.72 R² between profit margin and year-earlier customer satisfaction scores.*

**Review points**: Does the discussion tie back to the Introduction's research questions? Is each result explained? Are inferences overextended or are new concepts introduced abruptly? Is quantitative description used instead of vague qualitive language?

---

### 2.9 References (Principles)

References reflect academic integrity and traceability; each must correspond one-to-one with in-text citations.

**Review points**:

- Does the format match the target journal (author-year / numbered; punctuation, italics, DOI capitalisation)?
- Are ≥70% of references highly cited within 3–5 years? Is there appropriate citation of the target journal's own papers?
- Do in-text citations and the reference list match (no omissions, no extras, number correspondence)?
- Are there incorrect DOIs, missing volume/issue/pages, pirated/fabricated references?
- Do the references genuinely support the claims they are cited for (no misattribution)?

---

### 2.10 Acknowledgments and Statements

Acknowledgments reflect academic integrity and compliance; verify these five items one by one:

- **Funding**: are all funding sources and grant numbers listed (e.g., National Natural Science Foundation of China No. XXXXXXXX)?
- **Ethics approval**: for human/animal studies, is IRB/ethics committee approval number and informed consent noted?
- **Conflict of interest statement**: is any potential economic/non-economic conflict truthfully declared (even "no conflicts" must be stated, e.g., "The authors declare no conflicts of interest.")?
- **Acknowledgement completeness**: have individuals and institutions that provided substantive help (technical assistance, reagent provision, data support, language editing) but do not meet authorship criteria been acknowledged?
- **Authorship compliance**: no inappropriate署名 (individuals列入 without consent); no unauthorised acknowledgements (acknowledged party unaware/unconsenting).

**Review points**: are all five items complete? Are funding numbers accurate? Does the ethics approval number match? Is the COI declared?