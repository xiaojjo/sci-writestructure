# sci-writestructure
基于 IMRAD 结构骨架 + SCI 通用写作范式，对学术论文草稿做逐节诊断、严重程度评级与改写建议。
## 功能
- 原创性自检（4 问）
- 题目 / 摘要 / 关键词 / 引言 / 方法 / 结果 / 讨论 / 结论 / 致谢 / 参考文献 逐节审查
- 中英双语适用
- 先出审阅报告，经确认后再落盘改稿
## 如何拉取
```bash
git clone https://github.com/xiaojjo/sci-writestructure.git
```
## 文件结构
```
SKILL.md                       # Skill 主流程与执行规则
references/
  paper-criteria.md            # 原创性自检 + 各节原则
  sci-writing-standard.md      # 各节字数/句式公式、避雷点
  phrase-bank.md               # 英文句式模板
  discipline-templates.md      # 非生科学科 M&M 与指标措辞
```
## 使用方法
在 Hermes Agent 中引用本 skill 后，提交论文草稿或指定章节即可自动触发审阅流程。
## 适用学科
理工 / 文理 / 医学 / 农林 / 经管等 SCI 通用学科。
