# Government Document Workflow Skill

A Codex skill for drafting, reviewing, routing, and archiving Chinese government and public-sector administrative documents.

## What It Covers

- Official document drafting and rewriting
- Document type selection for the 15 party/government document types
- Format checks based on GB/T 9704-2012
- Review checklists for authority, purpose, structure, wording, and attachments
- Incoming/outgoing document workflows
- Countersignature, legal/compliance review, supervision, and archive metadata
- Operational work plans with leadership groups, member units, lead/support departments, special working groups, ledgers, graded response, traffic support, funding support, social impact assessment, and post-evaluation
- Printable PDF formatting guidance for GB/T 9704-style page geometry, official fonts, 22-line/28-character grids, and visual QA

## Current Rules Reference

The skill includes a current-format reference checked on 2026-06-11:

- GB/T 9704-2012《党政机关公文格式》: current on the National Public Service Platform for Standards
- GB/T 9704-1999《国家行政机关公文格式》: abolished on the National Public Service Platform for Standards
- 《党政机关公文处理工作条例》: used as the baseline document-handling procedure framework

For formal issuance, always verify against the issuing body's latest local templates and implementation rules.

## Install

Copy the skill folder into your Codex skills directory:

```bash
cp -R government-document-workflow ~/.codex/skills/
```

Then invoke it in Codex:

```text
Use $government-document-workflow to review this notice for format, authority, and workflow issues.
```

## Structure

```text
government-document-workflow/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── document-types.md
    ├── format-and-rules.md
    ├── operational-plans.md
    ├── pdf-formatting.md
    ├── process-patterns.md
    └── review-checklist.md
```
