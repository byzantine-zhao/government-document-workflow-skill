---
name: government-document-workflow
description: Draft, review, route, and archive Chinese government and public-sector administrative documents. Use when Codex is asked to handle official documents such as notices, requests for instructions, reports, replies, letters, meeting minutes, announcements, public notices, internal memos, approvals, circulation forms, document workflow design, receive/send document handling, countersignature, leader sign-off, supervision reminders, archive metadata, or compliance checks against administrative document conventions.
---

# Government Document Workflow

## Core Workflow

Use a conservative administrative-office style: accurate, concise, traceable, and procedure-aware.

1. Clarify the task type: drafting, rewriting, format review, workflow routing, supervision, archive indexing, or process design.
2. Identify the document class: notice, request for instructions, report, reply, letter, meeting minutes, announcement, public notice, decision, opinion, memo, or circulation note.
3. Check current-source assumptions in `references/format-and-rules.md` before giving format, procedure, or compliance advice.
4. Ask only for missing facts that materially affect legality, authority, recipients, dates, decisions, or process ownership. Otherwise proceed with marked assumptions.
5. Separate content work from process work. Draft or review the text first, then propose routing, approvals, deadlines, and archive metadata.
6. Flag high-risk issues plainly: missing authority, wrong recipient relationship, request/report mixing, unclear responsible department, missing legal basis, sensitive information, confidentiality level, or absent signature/date.

## Decision Map

- For drafting or rewriting official text, read `references/document-types.md`.
- For format, language, and compliance review, read `references/review-checklist.md`.
- For current format elements, fonts, page layout, document elements, and governing norms, read `references/format-and-rules.md`.
- For workflow routing, approvals, supervision, or archive fields, read `references/process-patterns.md`.

## Output Patterns

For drafting:

```markdown
【文种】...
【适用前提】...
【正文草案】
...
【需补充信息】...
【流程建议】...
```

For review:

```markdown
【总体判断】可用 / 需修改 / 不建议发出
【主要问题】
1. ...
【修改建议】
...
【修订稿】
...
```

For workflow design:

```markdown
【流程名称】...
【适用范围】...
【节点】拟稿 -> 审核 -> 会签 -> 合法性/合规审查 -> 签发 -> 编号印发 -> 督办 -> 归档
【角色与权限】...
【时限与提醒】...
【归档元数据】...
```

## Guardrails

- Do not invent laws, document numbers, approvals, departments, seals, signatures, or dates.
- Do not present legal compliance as guaranteed. Say "建议由法制/合规部门复核" when authority, law, procurement, personnel, discipline, finance, or citizen rights are affected.
- Preserve the user's political, institutional, and jurisdictional context. If unclear, use neutral wording such as "本单位" and "有关部门".
- Keep official wording direct. Prefer short sentences, concrete responsible parties, explicit deadlines, and measurable requirements.
- Avoid marketing tone, exaggeration, casual language, and unsupported evaluation.
- When documents may contain secrets, personal information, law-enforcement details, personnel decisions, tenders, or disciplinary matters, recommend confidentiality classification and access control review.
- For formal issuance in mainland China, tell the user to verify against the issuing body's latest local implementation rules and templates because many organs maintain detailed style sheets in addition to national rules.
