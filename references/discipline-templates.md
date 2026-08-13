# Discipline-specific Templates

This file supplements `sci-writestructure`'s **non-life-science discipline** templates so the skill covers its declared scope: STEM/CS, economics, humanities/social sciences.
Medicine / life sciences (cells, animals, IRB, expression levels, etc.) are already in `phrase-bank.md` and are not repeated here.

> Note: the M&M and metric phrasing below are AI-generated drafts per discipline conventions; **quality to be reviewed by the user**. Generic functional phrases (gap, method choice, result statement, conclusion, references) remain in `phrase-bank.md` Part B and are cross-disciplinary; this file only supplements **discipline-specific** method and metric phrasing.

---

## D1. STEM / CS / Engineering (Materials and Methods)

- **Datasets / data sources**:
  - `The dataset consists of ... samples collected from ..., spanning the period ... to ....`
  - `We evaluated on the public ... benchmark (e.g., ImageNet / SQuAD / ...), which contains ... .`
  - `Raw signals were acquired at a sampling rate of ... Hz using ... .`
- **Experimental environment / hardware & software**:
  - `All experiments were conducted on a machine with an ... GPU, ... CPU, and ... GB RAM, using ... (framework, version).`
  - `The simulation was performed in ... with parameters ... .`
- **Algorithms / models**:
  - `We propose a ... model based on ..., implemented in ... .`
  - `The network was trained with the ... optimizer, initial learning rate ..., batch size ..., for ... epochs.`
- **Evaluation metrics**:
  - `Performance was evaluated using accuracy, precision, recall, F1-score, and AUC.`
  - `Prediction error was measured by MSE / MAE / RMSE.`
  - `Structural performance was assessed via ... (e.g., strength, efficiency, latency).`
- **Reproducibility**:
  - `The source code and trained weights are available at ... .`
  - `Random seeds were fixed at ... across ... independent runs for reproducibility.`
- **Statistics / significance**:
  - `Results are reported as mean ± SD over ... runs. Significance was assessed via ... test (p < 0.05).`

## D2. Economics / Business (Materials and Methods)

- **Data sources**:
  - `Firm-year observations were drawn from the ... database (e.g., CSMAR / Compustat) for the period ... to ....`
  - `We obtained ... from ..., covering ... entities / countries.`
- **Sample selection**:
  - `After excluding ... and requiring non-missing values for all variables, the final sample comprises ... observations.`
- **Model specification**:
  - `We estimate ... using a fixed-effects panel regression: Y_it = β₀ + β₁X_it + ... + ε_it.`
  - `Endogeneity was addressed via ... (instrumental variable / 2SLS / difference-in-differences / RDD).`
- **Variable definition**:
  - `The dependent variable ... is defined as ...; the key independent variable ... proxies for ....`
- **Robustness**:
  - `We conduct ... robustness checks (alternative measures, subsample analysis, placebo test).`

## D3. Agriculture / Forestry (Materials and Methods)

- **Experimental site / materials**:
  - `Field experiments were conducted at ... (latitude ..., longitude ...), with soil type ....`
  - `Seeds of ... were sown on ... at a density of ... .`
- **Treatment design**:
  - `A randomized complete block design with ... treatments and ... replicates was adopted.`
  - `Seedlings were subjected to ... stress (e.g., drought / salinity) by ....`
- **Measured indicators**:
  - `Plant height, leaf area, and biomass were measured at ....`
  - `Soil moisture, pH, and nutrient content were determined using ....`
- **Data analysis**:
  - `Data were analyzed by ANOVA (p < 0.05); means were separated by ... test.`

## D4. Humanities / Social Sciences (Materials and Methods)

- Note: `phrase-bank.md` Part B already contains case-study, survey, semi-structured interview, qualitative phrases; this section supplements discipline-specific sources.
- **Texts / archives**:
  - `A corpus of ... documents (...–...) was compiled from ... and analyzed via thematic / discourse analysis.`
- **Questionnaires**:
  - `A structured questionnaire with ... items (Cronbach's α = ...) was distributed to ...; ... valid responses were returned.`
- **Secondary data**:
  - `Secondary data were extracted from ... (e.g., World Bank / ...), covering ....`
- **Ethics**:
  - `Ethical approval was obtained from ...; informed consent was secured from all participants.`

## D5. Cross-disciplinary cautions (non-life-science Results / Abstract phrasing)

- When the manuscript is non-life-science, **avoid life-science-specific terms** (expression / secretion levels, animal / cell, etc.); use generic measures: `values, scores, metrics, estimates, coefficients, error rates, accuracies`.
- **Abstract result sentences (universally套able)**:
  - `Compared with the baseline, the proposed method achieved a ...% improvement in ....`
  - `The ... coefficient is significantly positive (β = ..., p < ...), indicating ....`
  - `Across ... conditions, ... consistently outperformed ... by ....`
- **Results objective statements (generic)**:
  - `As shown in Fig. ..., ... increased from ... to ... under ....`
  - `Table ... reports that the gap between ... and ... narrowed by ....`

---

## Discipline → Template Routing Table

| Discipline | M&M primary template | Metric / result phrasing |
|------------|---------------------|--------------------------|
| Medicine / Life sciences | phrase-bank `A4` | phrase-bank `A5` / `B8` |
| STEM / CS / Engineering | discipline-templates `D1` | D1 metrics + D5 |
| Economics / Business | discipline-templates `D2` | D2 variables/coefficients + D5 |
| Agriculture / Forestry | discipline-templates `D3` | D3 measurements + D5 |
| Humanities / Social Sciences | discipline-templates `D4` + phrase-bank social-science phrases | D5 |