# Simple Academic Writing

A reusable Codex skill for planning, drafting, revising, and reviewing long-form professional writing. It is designed for academic papers, technical and research reports, proposals, literature reviews, quantitative results analyses, and achievement summaries.

The skill organizes writing around a central claim, a reader-oriented argument chain, and evidence appropriate to each claim. It also provides genre-specific guidance, quantitative evidence and visualization standards, and a final review checklist.

## What it changes

- Starts from purpose, audience, and the central claim rather than the order of available material.
- Builds a need–challenge–gap–solution–mechanism–evidence–implication argument chain.
- Matches claims to theory, data, literature, cases, or analysis.
- Removes work-log narration, revision commentary, empty praise, and defensive disclaimers.
- Separates the roles of prose, figures, and tables.
- Adapts the argument to papers, reports, proposals, reviews, evaluations, and summaries.

## Repository structure

```text
.
|-- SKILL.md
|-- agents/
|   `-- openai.yaml
|-- references/
|   |-- deliverable-modes.md
|   |-- evidence-and-visuals.md
|   `-- review-checklist.md
|-- GUIDE_ZH.md
`-- LICENSE
```

- `SKILL.md` contains the shared workflow and decision rules.
- `references/` is loaded progressively according to the writing task.
- `GUIDE_ZH.md` is the complete Chinese human-readable standard.

## Install

Clone the repository and copy the skill files into a folder named `professional-writing` under your Codex skills directory.

### PowerShell

```powershell
git clone https://github.com/Jsyhw/SimpleAcademicWriting.git
$target = Join-Path $env:USERPROFILE ".codex\skills\professional-writing"
New-Item -ItemType Directory -Force -Path $target | Out-Null
Copy-Item .\SimpleAcademicWriting\SKILL.md $target
Copy-Item .\SimpleAcademicWriting\agents $target -Recurse
Copy-Item .\SimpleAcademicWriting\references $target -Recurse
```

### Bash

```bash
git clone https://github.com/Jsyhw/SimpleAcademicWriting.git
mkdir -p ~/.codex/skills/professional-writing
cp SimpleAcademicWriting/SKILL.md ~/.codex/skills/professional-writing/
cp -R SimpleAcademicWriting/agents SimpleAcademicWriting/references ~/.codex/skills/professional-writing/
```

## Use

Invoke it explicitly:

```text
Use $professional-writing to plan, draft, or revise this professional document.
```

中文示例：

```text
使用 $professional-writing 规划、撰写或修订这份专业文稿。
```

Implicit invocation is enabled, so Codex can also select the skill automatically for relevant long-form professional writing tasks.

## Design principles

The skill deliberately keeps the shared entry point compact. Detailed rules are loaded only when needed:

- deliverable-specific argument structures;
- evidence, statistics, figures, and tables;
- final logical, linguistic, citation, and layout review.

This prevents conventions from one paper or discipline from becoming universal requirements for unrelated writing.

## License

MIT
