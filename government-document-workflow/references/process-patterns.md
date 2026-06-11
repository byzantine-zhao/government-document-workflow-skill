# Process Patterns

Use this reference for official document workflow design, routing, supervision, and archiving. The 2012 party/government document handling rules distinguish 公文拟制, 发文办理, 收文办理, and 整理归档.

## Incoming Document Handling

Typical nodes:
1. 签收
2. 登记
3. 初审
4. 承办
5. 传阅
6. 催办
7. 答复
8. Result confirmation
9. Closure and archive

Key fields:
- Receipt number
- Original sender
- Received date
- Title
- Urgency
- Confidentiality level
- Proposed handling department
- Leader instruction
- Deadline
- Result summary
- Archive category

## Outgoing Document Handling

Typical nodes:
1. Draft by responsible department
2. Department head review
3. Office format and wording review
4. Countersignature by related departments
5. Legal/compliance review when needed
6. Leader sign-off
7. 复核
8. 登记
9. 印制
10. 核发/分发
11. Disclosure review if public-facing
12. Archive

Controls:
- Draft owner and version history
- Required review roles by document type
- Redline or comment record for major changes
- Approval record before numbering and seal
- Dispatch list and receipt confirmation

## Supervision And Reminder Rules

Use deadline levels:
- Urgent: same day or 1 working day
- Normal: 3 to 5 working days
- Complex: define milestone dates

Reminder pattern:
- First reminder before deadline
- Escalation on overdue
- Written reason required for extension
- Closure only after result is accepted by the assigning office

## Archive Metadata

Recommended fields:
- Document title
- Document type
- Document number
- Issuing body
- Main recipient
- Copy recipients
- Drafting department
- Signatory
- Issue date
- Effective date
- Confidentiality level
- Urgency
- Retention period
- Keywords
- Related matter/project
- Workflow instance id
- Final PDF/Word file
- Attachments
- Approval record

## Procedure Integrity

- 公文拟制: 起草, 审核, 签发.
- 发文办理: 复核, 登记, 印制, 核发.
- 收文办理: 签收, 登记, 初审, 承办, 传阅, 催办, 答复.
- 整理归档: collect final text, attachments, approval records, dispatch/receipt evidence, and handling result; lock the final version after dispatch.

## Workflow Risk Controls

- Add legal/compliance review for policy, contract, procurement, personnel, finance, penalty, license, citizen rights, public disclosure, or data sharing matters.
- Add confidentiality review before external dispatch or public release.
- Require countersignature when responsibilities cross departments.
- Require archive lock after dispatch to preserve the final version.
- Keep a visible audit trail for drafting, review, sign-off, numbering, sealing, dispatch, and closure.
