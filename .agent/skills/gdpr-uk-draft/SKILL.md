---
name: gdpr-uk-draft
description: Draft and review UK GDPR compliance documents from the repository's full templates, including privacy notices, records of processing activities, processor agreements, DPIAs, LIAs, transfer risk assessments, and breach notifications. Use when Codex must draft, write, create, review, or check a UK privacy or data-protection document, or explain what it must contain, with citations to UK GDPR, DPA 2018, DUAA 2025, and ICO guidance.
---

# UK GDPR Document Drafting

Determine the requested document and facts from the current user message. If the document type is missing, ask which document is needed.

Resolve all paths relative to this skill directory. Read `../../../references/legal-framework.md` and `../../../references/duaa-2025-changes.md` before drafting, then use the matching source:

| Document | Source | Authority |
|---|---|---|
| Privacy notice | `../../../templates/privacy-notice.md` | Arts 12-14 |
| Controller RoPA | `../../../templates/ropa-controller.md` | Art 30(1) |
| Processor RoPA | `../../../sources/ico-ropa-template-processor.xlsx` | Art 30(2) |
| DPIA | `../../../templates/dpia.md`; compare `../../../sources/ico-dpia-example-completed.pdf` when useful | Art 35 |
| Processor agreement | `../../../templates/processor-agreement.md` | Art 28(3) |
| LIA | `../../../templates/lia.md` | Art 6(1)(f) |
| ICO breach notification | `../../../templates/breach-notification-ico.md` | Art 33 |
| Individual breach notification | `../../../templates/breach-notification-individuals.md` | Art 34 |
| Transfer risk assessment | `../../../templates/tra.md` | Art 46 as amended by DUAA 2025 |
| International-transfer instrument | `../../../sources/ico-idta.pdf` or `../../../sources/ico-addendum.pdf` | Art 46; DPA 2018 s.119A |

Do not improvise international-transfer clauses; populate the official instrument's tables.

## Workflow

1. Gather facts in one focused round: controller identity, purposes, data categories, special-category or criminal-offence data, recipients and processors, non-UK destinations, retention, and whether children are in scope.
2. Instantiate the template. Replace placeholders with supplied facts. Never invent organisational facts. Leave unknowns as `[TO CONFIRM: ...]`, remove inapplicable sections, and explain what was removed and why. Retain legal citations unless the user asks for a clean copy.
3. Run the template's reviewer checklist and report every item as satisfied or outstanding.
4. For an existing document, compare it against the matching template and cited provisions. Report gaps as `missing or deficient item -> authority -> suggested wording`.
5. Close every produced document with the standing note below.

## Rules

- Cite the specific article or section beside each substantive section.
- Apply UK GDPR and DPA 2018 as amended by DUAA 2025. Flag EU divergences when EU law may also apply.
- For a live breach, produce the Art 33 notification content before polishing other material because the 72-hour clock may be running.
- Keep facts consistent across privacy notices, RoPAs, DPIAs, processor agreements, and breach communications.
- Verify current, high-stakes legal points against official legislation.gov.uk or ico.org.uk sources.

## Standing note

> This document was generated from the gdpr-uk templates and the facts you provided. It is a working draft, not legal advice: have your Data Protection Officer or legal counsel review it before adoption or publication, and resolve every `[TO CONFIRM]` marker first.
