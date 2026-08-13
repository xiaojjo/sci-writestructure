# Paper Revision (sci-writestructure)

Hermes Agent skill: diagnoses and revises academic manuscript drafts section by section based on the IMRAD skeleton and universal SCI writing standards.

## Features

- Originality self-check (4 questions)
- Section-by-section review: Title, Abstract, Keywords, Introduction, Methods, Results, Discussion, Conclusion, Acknowledgments, References
- Works for both Chinese and English drafts
- Produces review report first; edits applied only after user confirmation

## Installation

```bash
git clone https://github.com/xiaojjo/sci-writestructure.git
```

## File structure

```
SKILL.md                       # Main workflow and execution rules
references/
  paper-criteria.md            # Originality self-check + section principles
  sci-writing-standard.md      # Per-section word counts, sentence formulae, pitfalls
  phrase-bank.md               # English sentence skeletons
  discipline-templates.md      # Non-life-science M&M and metric phrasing
```

## Usage

Invoke this skill in Hermes Agent, then submit a manuscript draft or specify a section to trigger the review workflow automatically.

## Applicable disciplines

STEM / Humanities / Medicine / Agriculture / Economics — universal SCI disciplines.