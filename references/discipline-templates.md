# 非生命科学学科模板 (Discipline-specific Templates)

本文件补充 `sci-writestructure` 的**非生命科学学科**模板，使 skill 覆盖其声明的「理工 / 文理 / 医学 / 农林 / 经管」全学科。
医学 / 生科（细胞、动物、IRB、表达量等）已在 `phrase-bank.md`，此处不重复。

> 说明：以下 M&M 与指标句式由 AI 按各学科通行写法自拟，**质量待用户审**。通用功能短语（gap、方法选择、结果陈述、结论、参考文献等）仍见 `phrase-bank.md` 的 B 部，跨领域通用；本文件只补**学科专属**的方法与指标措辞。

---

## D1. 理工科 / CS / 工程（Materials and Methods）

- **数据集 / 数据来源**：
  - `The dataset consists of ... samples collected from ..., spanning the period ... to ....`
  - `We evaluated on the public ... benchmark (e.g., ImageNet / SQuAD / ...), which contains ... .`
  - `Raw signals were acquired at a sampling rate of ... Hz using ... .`
- **实验环境 / 软硬件**：
  - `All experiments were conducted on a machine with an ... GPU, ... CPU, and ... GB RAM, using ... (framework, version).`
  - `The simulation was performed in ... with parameters ... .`
- **算法 / 模型**：
  - `We propose a ... model based on ..., implemented in ... .`
  - `The network was trained with the ... optimizer, initial learning rate ..., batch size ..., for ... epochs.`
- **评价指标**：
  - `Performance was evaluated using accuracy, precision, recall, F1-score, and AUC.`
  - `Prediction error was measured by MSE / MAE / RMSE.`
  - `Structural performance was assessed via ... (e.g., strength, efficiency, latency).`
- **可复现性**：
  - `The source code and trained weights are available at ... .`
  - `Random seeds were fixed at ... across ... independent runs for reproducibility.`
- **统计 / 显著性**：
  - `Results are reported as mean ± SD over ... runs. Significance was assessed via ... test (p < 0.05).`

## D2. 经管 / 经济（Materials and Methods）

- **数据来源**：
  - `Firm-year observations were drawn from the ... database (e.g., CSMAR / Compustat) for the period ... to ....`
  - `We obtained ... from ..., covering ... entities / countries.`
- **样本筛选**：
  - `After excluding ... and requiring non-missing values for all variables, the final sample comprises ... observations.`
- **模型设定**：
  - `We estimate ... using a fixed-effects panel regression: Y_it = β₀ + β₁X_it + ... + ε_it.`
  - `Endogeneity was addressed via ... (instrumental variable / 2SLS / difference-in-differences / RDD).`
- **变量定义**：
  - `The dependent variable ... is defined as ...; the key independent variable ... proxies for ....`
- **稳健性**：
  - `We conduct ... robustness checks (alternative measures, subsample analysis, placebo test).`

## D3. 农林（Materials and Methods）

- **试验地 / 材料**：
  - `Field experiments were conducted at ... (latitude ..., longitude ...), with soil type ....`
  - `Seeds of ... were sown on ... at a density of ... .`
- **处理设计**：
  - `A randomized complete block design with ... treatments and ... replicates was adopted.`
  - `Seedlings were subjected to ... stress (e.g., drought / salinity) by ....`
- **测定指标**：
  - `Plant height, leaf area, and biomass were measured at ....`
  - `Soil moisture, pH, and nutrient content were determined using ....`
- **数据分析**：
  - `Data were analyzed by ANOVA (p < 0.05); means were separated by ... test.`

## D4. 文科 / 社科（Materials and Methods）

- 注：`phrase-bank.md` B 部已含 case-study、survey、semi-structured interview、qualitative 等句式，此处补其专属来源。
- **文本 / 档案**：
  - `A corpus of ... documents (...–...) was compiled from ... and analyzed via thematic / discourse analysis.`
- **问卷**：
  - `A structured questionnaire with ... items (Cronbach's α = ...) was distributed to ...; ... valid responses were returned.`
- **二手数据**：
  - `Secondary data were extracted from ... (e.g., World Bank / ...), covering ....`
- **伦理**：
  - `Ethical approval was obtained from ...; informed consent was secured from all participants.`

## D5. 跨学科技法注意（非生科 Results / Abstract 措辞）

- 当稿件非生科时，**避免生科专属词**（expression / secretion levels、animal / cell 等），改用通用度量：`values, scores, metrics, estimates, coefficients, error rates, accuracies`。
- **Abstract 结果句（通用可套）**：
  - `Compared with the baseline, the proposed method achieved a ...% improvement in ....`
  - `The ... coefficient is significantly positive (β = ..., p < ...), indicating ....`
  - `Across ... conditions, ... consistently outperformed ... by ....`
- **Results 客观陈述（通用）**：
  - `As shown in Fig. ..., ... increased from ... to ... under ....`
  - `Table ... reports that the gap between ... and ... narrowed by ....`

---

## 学科 → 模板路由

| 学科 | M&M 主模板 | 指标 / 结果措辞 |
|------|------------|------------------|
| 医学 / 生科 | phrase-bank `A4` | phrase-bank `A5` / `B8` |
| 理工 / CS / 工程 | discipline-templates `D1` | D1 评价指标 + D5 |
| 经管 / 经济 | discipline-templates `D2` | D2 变量/系数 + D5 |
| 农林 | discipline-templates `D3` | D3 测定 + D5 |
| 文科 / 社科 | discipline-templates `D4` + phrase-bank 社科短语 | D5 |
