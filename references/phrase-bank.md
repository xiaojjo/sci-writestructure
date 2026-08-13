# Academic Phrase Bank

This file is the sentence-reference library for the `sci-writestructure` skill, used alongside `sci-writing-standard.md`.
Purpose: during Step 2 section-by-section review and Step 3 producing "revision suggestions", retrieve English sentence skeletons appropriate for the section/function, substitute variables, and present usable suggestions (author can use directly, but never copy template example sentences verbatim).

**Retrieval tip**: search by section name (e.g., `A3`, `Discussion`, `gap`) or functional keywords (e.g., `However`, `hypothesized`, `consent`).

> **Usage boundary (important)**: this library provides **sentence structure references only** — borrow skeletons and substitute variables. All `XXX`/`X`/`Y` and ellipsis places must be filled with the author's actual manuscript content. A few example sentences in the library with specific content (e.g., `Because of the rarity of this cancer…`) are illustrative only — **replace with the author's actual research subject when套用**; never copy verbatim into the manuscript. See SKILL.md quality criterion "No verbatim template copying".

---

## A. Section-by-section Sentence Skeletons

### A1. Title

- `XXX attenuates XXX-induced XXX disease through/by the inhibition/regulation of XX`

### A2. Abstract

**Structural framework**: one fluent paragraph, four functional components naturally connected. Not a segmented format.

1) **Opening (1 sentence)**: use a factual statement to pinpoint the research background and gap. Avoid empty importance claims. Recommended: "consensus → But → controversy/gap" or "fact → yet → uncertainty" contrast structure.
2) **Method/approach (1 sentence)**: fixed skeleton `Here we [verb] + [precise research scope, sample size, method]`. This sentence only states what was done; do not preview conclusions.
3) **Findings (2–4 sentences, ≥60% of length)**: state core findings one by one in logical order. Can include转折, contrast, quantified data. Use first/second/finally or however/whereas/in contrast for natural transition. Each finding must include treatment, effect direction, magnitude, and comparison baseline at minimum.
4) **Closing inference (1 sentence)**: make a specific inference from findings. Do not write "further studies are needed" or "These results highlight the importance of..." — either write a concrete scientific inference or what the study implies for other fields. The closing sentence leaves the reader with a conclusion, not a声明.

**Formatting conventions**:

- Write out numbers on first use ("around 2,300 insect species"); numerals thereafter.
- Space between unit and number (0.5 °C min⁻¹, not 0.5°C min⁻¹).
- Statistical significance in parentheses (p < 0.05); CI as `(95% CI = lower, upper)`.
- Write out full term on first abbreviation.

**Real-paper fragments (structural reference only, not copyable)**:

- 2026 Nature insect heat tolerance: opening "Insects make up the majority of all animal species, with 70% occurring in the tropics, yet the impacts of warming on tropical insects remain highly uncertain." → method "Here we compared... around 2,300 insect species along... elevational gradients and identified genomic signatures across the insect tree of life." → findings "We show that... do not proportionally track environmental temperatures but approach an asymptote in... Heat tolerance showed strong differences among insect orders and families, reflected in..." → closing "Our data suggest a limited capacity of insects in the Earth's most biodiverse regions to buffer future warming."
- 2004 Nature Inner Mongolia grassland: opening "Numerous studies have suggested that... But this view has been challenged." → method "On the basis of a 24-year study... here we present three key findings." → findings "First, that...; second, that...; and finally, that..." → closing "Our study provides new insights for better management and restoration of the rapidly degrading Inner Mongolia grassland."
- 2015 Nature grassland diversity rebound: opening "The negative effect of... is now incontrovertible. However, the degree to which... can be expected to bounce back is uncertain." → method "Here we present evidence from the 160-year-old Park Grass Experiment..." → findings "The proportion of legumes, species richness and diversity increased... Plots that stopped receiving N fertilizer recovered much of the diversity..." → closing "There was no evidence that chronic N addition has resulted in an alternative low biodiversity state..."

### A3. Introduction

1) **Background Known** (General → specific).
2) **Unknown / gap** (how to fill, why it matters):
   - `Until now, it has not been possible to identify ….`
   - `However, we do not know what effect this treatment will have on ….`
   - `There has been some disagreement, however, in the findings with this model….`
   - `So far, only qualitative findings have been obtained…`
   - `Because of the rarity of this cancer, it has been difficult to determine survival rates with statistical certainty…`
3) **Hypothesis**:
   - `The purpose of our study was to determine ….`
   - `We hypothesized that ….` / `Our hypothesis was that….`
4) **Strategy**:
   - `We tested our hypothesis by examining….`
   - `To do this, we used … and analyzed … in an in situ model ….`
   - `To evaluate/investigate/explore the inhibitory/regulatory effect of … on …., the … assay/methods/experiments were employed/used.`
5) **Conclusion**:
   - `Overall, our findings that … confirm/indicate/suggest/demonstrate ….`
   - `In this study / In the present study, we found/observed/demonstrated that ….`

### A4. Materials and Methods

1) **Materials and reagents**: drugs, reagents, equipment, antibodies, etc.
2) **Cell lines and cultures**: which cells? supplier? how prepared/cultured/treated/grouped? how collected?
3) **Human subjects**: IRB approval; informed consent; source of study population; inclusion/exclusion criteria; sample collection and number.
4) **Animals**: standards of animal care; supplier; how many; how treated/grouped/killed; how samples collected (time points, volume, gram, surgery).
5) **Experiment 1–4**: `To evaluate/examine/determine/detect/assess/measure …., we performed … assay/experiment.` + what was done and why.
6) **Statistical tests/analysis**: comparisons/evaluation used; which tests; significance levels; software.

### A5. Results

**Paragraph structure (loop per paragraph)**: topic sentence states the finding → data support (value + statistics) → interaction/exception (if applicable) → figure/table citation. One core finding per paragraph; transition between paragraphs by switching indicator or factor.

- **Subheading suggestion**: `Effect of … on … in ….` or directly named after the indicator; avoid vague titles.
- **Topic sentence**: first sentence directly states the paragraph's core conclusion — treatment → indicator → effect direction → magnitude. No beating around the bush.
- **Data support**: follows immediately after topic sentence. Depends on analysis type; use the corresponding statistical format (see below "Statistical reporting format reference").
- **Interaction/exception**: multi-factor experiments must report main effects and interaction effects (significant/not significant/marginal). When decomposing by year/time, state in chronological order.
- **Figure/table citation**: at the end of the data-support sentence in parentheses: (Figure X, Table Y). Or asynchronous citation ("as shown in Figure X").
- **Paragraph-end summary** (optional): only when needed to summarise composite findings; avoid writing "Taken together" in every paragraph.

**Statistical reporting format reference** (format conventions for each method — not fill-in templates; fill with actual values):

- **ANOVA / linear models**: report `F(effect df, residual df) = value, P = value`
- **GLM / logistic regression**: report `χ²(df) = value, P = value`
- **Effect size + CI**: report `effect size (95% CI = lower, upper)` — CI not containing 0 indicates significance
- **Regression coefficients**: report `β = value; 95% CI = lower, upper`; optionally append P value
- **t-test**: report `t(df) = value, P = value; mean difference = value (95% CI = lower, upper)`
- **Survival analysis**: report `HR = value, 95% CI = lower, upper, P = value`
- **Between-group comparisons (post-hoc)**: present with letter-marking method or difference + CI; treatments sharing a letter are not significantly different
- **Selection coefficient**: report `s = value`
- **Phylogenetic signal**: report `Pagel's λ = value, P = value; Blomberg's K = value, P = value`
- **Non-significant results**: explicitly note `P > 0.05` or CI crossing zero; can also note trend direction

**Real-paper fragments (structural reference only)**:

- 2026 Nature insect heat tolerance: "...the thermal tolerance range across the whole insect community did not significantly change with elevation (Neotropics: estimate = 0.00036, F₁,₂₃ = 1.785, P = 0.195... Afrotropics: estimate = 0.00003, F₁,₁₃ = 0.004, P = 0.951)."
- 2022 Nature Comms insect heat plasticity: "For every 1 °C rise in acclimation temperature, CTmax increased by 0.091 °C (95% CI = 0.030, 0.153)."
  - Same paper, non-significant report: "we found no relationship between latitude and ARR (CTmax βARR = −0.001; 95% CI = −0.002, 0.001)."
- 2025 ES&T pesticide tolerance: "Chlorpyrifos decreased survival in sensitive clones (−10.1%, P = 0.023 at low; −30.5%, P < 0.001 at high), while it did not affect tolerant clones (both concentrations: P > 0.60) (Figure 2)."
- Your original text (nitrogen addition study): "Both year and N addition significantly affected species richness, however, no significant interactions were detected (Table 1)."

### A6. Discussion (paragraph order)

1) **Conclusion** (based on main findings, tie back to purpose/hypothesis, first paragraph):
   - `Our findings that … confirm ….` / `In this study, we found that …` / `Our results indicate/suggest/show that ….`
2) **Interpretation**: further explain, helping readers understand the research importance.
3) **Fit with literature**:
   - Consistent: `Our data are consistent with ….` / `Our findings on … agree with those reported by … et al., who …..`
   - Contradictory: `Our data differ from …` / `Unlike … et al., we observed that ….`
4) **Novelty / strength** (optional): `In this study, we showed for the first time that ….` / `The major strength of this study was …`
5) **Limitation**: `Our study subjects were …, so it is not known whether our results are applicable to groups….` / `Our study had several limitations. First …..`
6) **Generalizations**: `Although our cohort was limited to …, the results suggest that …`
7) **Why gap matters**: `Our findings will allow us to take the next step in ….`
8) **Implications / speculation**: `Our findings may be useful in ….` / `We speculate that …` / `Our results imply that … but this must be tested further ….` / `These findings are important for … and point to the need for …`
9) **Avenues for further study**: `The next step is to …` / `Additional studies are needed to confirm …` / `Larger studies with longer follow-up are needed to …`

### A7. Acknowledgments

- `This study was supported by XXX; we thank Dr. XXX for XXX support/help.`
- `Disclosures: The authors have no financial conflicts of interest.`

### A8. Tables and Figures

- Tables: Table 1, Table 2…; Figures: Figure 1, Figure 2, Figure 3…
- Figure legend: `Figure 1: …..`

---

## B. Functional Phrase Bank (Cross-section)

### B1. Describing the field / importance — Applicable: Abstract (background), Introduction

1. It is becoming increasingly difficult to ignore the .......
2. X is the leading cause of death in western industrialised countries.
3. The issue of X has received considerable critical attention.
4. Central to the entire discipline of X is the concept of .......
5. X is at the heart of our understanding of .......

### B2. Emphasising a major problem in the field — Applicable: Introduction

1. However, a major problem with this kind of application is .......
2. Lack of X has existed as a health problem for many years.
3. Despite its safety and efficacy, X suffers from several major drawbacks:
4. However, research has consistently shown that first-year students have not attained an adequate understanding of ....... There is increasing concern that some Xs are being disadvantaged .......
5. Questions have been raised about the safety of prolonged use of .......

### B3. Emphasising controversy in the field — Applicable: Introduction, Discussion

1. To date there has been little agreement on what .......
2. More recently, literature has emerged that offers contradictory findings about .......
3. In many Xs a debate is taking place between Ys and Zs concerning .......
4. Debate continues about the best strategies for the management of .......
5. This concept has recently been challenged by ....... studies demonstrating .......

### B4. Emphasising knowledge gaps — Applicable: Introduction

1. Little is known about X and it is not clear what factors .......
2. What is not yet clear is the impact of X on .......
3. However, there have been no controlled studies which compare differences in .......
4. No previous study has investigated X.
5. Although extensive research has been carried out on ...., no single study exists which .... ..

### B5. Emphasising shortcomings of previous research — Applicable: Introduction

1. Most studies in the field of X have only focussed on .......
2. The experimental data are rather controversial, and there is no general agreement about .......
3. However, few writers have been able to draw on any structured research into the opinions and attitudes of .......
4. Although extensive research has been carried out on X, no single study exists which adequately covers .......
5. X's analysis does not take account of ..... nor does he examine .......

### B6. Describing methods (comparing methods / justifying choice) — Applicable: Materials and Methods

- Comparing methods:
  1. To date various methods have been developed and introduced to measure X:
  2. A variety of methods are used to assess X. Each has its advantages and drawbacks.
- Justifying a chosen method:
  3. The semi-structured approach was chosen because .......
  4. The X method is one of the more practical ways of .......
  5. It was considered that quantitative measures would usefully supplement and extend the qualitative analysis.
  6. Many of the distributions were not normal so non-parametric signed rank tests were run.

### B7. Describing experimental methods / sample characteristics / procedures — Applicable: Methods, Results

- Special methods:
  1. Article references were searched further for additional relevant publications. Articles were searched from January 1965 until April 2008.
  2. X was prepared according to the procedure used by Patel et al. (1957).
  3. For this study the X was used to explore the subsurface .......
- Sample characteristics:
  4. The initial sample consisted of 200 students of whom 13 did not complete all of the interviews.
  5. Two groups of subjects were interviewed, namely X and Y. The first group were .......
  6. Eligibility criteria required individuals to have received ....
  7. Five individuals were excluded from the study on the basis of ....
- Experimental procedures (purpose clause):
  8. To control for bias, measurements were carried out by another person.
  9. To determine whether ......., KG-1 cells were incubated for .......
- Experimental procedures (other):
  10. For the purpose of height measurement, subjects were asked to stand .......

### B8. Discussion: background information and result statement — Applicable: Discussion

- Background information:
  1. A strong relationship between X and Y has been reported in the literature.
  2. As mentioned in the literature review, .......
  3. The present study was designed to determine the effect of .......
- Stating results:
  4. The results of this study show/indicate that .......
  5. The most interesting finding was that .......
  6. In the current study, comparing X with Y showed that the mean degree of .......

### B9. Conclusion: summarising / restating purpose — Applicable: Conclusion

- Summarising:
  1. This paper has given an account of and the reasons for the widespread use of X .......
  2. This dissertation has investigated .......
- Restating purpose:
  3. This study set out to determine .......
  4. The purpose of the current study was to determine .......
  5. Returning to the hypothesis/question posed at the beginning of this study, it is now possible to state that .......

### B10. Reference-related phrases — Applicable: throughout

- Literature overview:
  1. There is a large volume of published studies describing the role of .......
  2. A large and growing body of literature has investigated .......
- Previous studies / academic activity:
  3. Many historians have argued that ....... (e.g. Jones, 1987; Johnson, 1990; Smith, 1994)
  4. Previous studies have reported ....... (Smith, 1985; Jones, 1987; Johnson, 1992).
  5. A number of studies have found that ....... (Smith, 2003; Jones, 2004).
  6. The relationship between X and Y has been widely investigated (Smith, 1985; Jones, 1987).

### B11. Research questions, hypotheses, method sources, limitations, frameworks, terminology — Applicable: Introduction, Methods, Discussion

- Research questions / hypotheses:
  1. The central question in this dissertation asks how .......
  2. The hypothesis that will be tested is that .......
  3. This study aimed to address the following research questions:
- Method / data sources:
  4. This study was exploratory and interpretative in nature.
  5. Both qualitative and quantitative methods were used in this investigation.
  6. The research data in this thesis is drawn from four main sources: .......
- Stating limitations:
  7. Due to practical constraints, this paper cannot provide a comprehensive review of ....... It is beyond the scope of this study to examine the .......
- Research framework:
  8. The overall structure of the study takes the form of six chapters, including this introductory chapter.
  9. The final chapter draws upon the entire thesis, tying up the various theoretical and empirical strands in order to .......
- Explaining key terms:
  10. While a variety of definitions of the term X have been suggested, this dissertation will use the definition first suggested by .......
  11. Throughout this paper the term X will refer to / will be used to refer to .......

### B12. Article focus: theoretical / methodological issues and limitations — Applicable: Discussion

- Theoretical level:
  1. One question that needs to be asked, however, is whether .......
  2. A serious weakness with this argument, however, is that .......
  3. The key problem with this explanation is that .......
  4. X's analysis does not take account of ..... nor does he examine .......
- Methodological level:
  5. Another problem with this approach is that it fails to take X into account.
  6. One major drawback of this approach is that .......

### B13. Literature introduction (general) — Applicable: Introduction (literature review)

1. Recently investigators have examined the effects of X on Y.
2. In the past two decades a number of researchers have sought to determine .......
3. Recent evidence suggests that .......
4. A number of researchers have reported .......
5. What we know about X is largely based upon empirical studies that investigate how .......

---

## C. Supplementary Phrases by Section (English)

Curated high-quality sentences from the original phrase bank, reorganised by article section.

### C1. Introduction

- `However, the evidence for this relationship is inconclusive ....`
- `This indicates a need to understand the various perceptions of ... that exist among ...`
- `The existing accounts fail to resolve the contradiction between X and Y.`
- `X is an important component in Y, and plays a key role in Z.`

### C2. Methods

- `A random sample of patients with ... was recruited from ...`
- `Eligible ... who matched the selection criteria were identified by ...`
- `... are the main non-invasive method used to determine ...`

### C3. Results

- `X provided the largest set of significant clusters of ...`
- `This experiment did not detect any evidence for .......`

### C4. Discussion

- `In reviewing the literature, no data was found on the association between X and Y.`
- `The main limitation of this method, however, is ...`
- `All the studies reviewed so far, however, suffer from the fact that .......`
- `This study set out with the aim of assessing the importance of X in .......`

### C5. Conclusion

- `This study has argued that X is the best instrument to .......`
- `This project was undertaken to design ... and evaluate ...`