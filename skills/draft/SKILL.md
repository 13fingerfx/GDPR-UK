---
name: draft
description: Drafts UK GDPR compliance documents from full templates — privacy notices, records of processing activities (RoPA), data processing agreements (DPAs), data protection impact assessments (DPIAs), legitimate interests assessments (LIAs), and personal data breach notifications (to the ICO and to individuals). Use when the user asks to draft, write, create, review, or check any privacy/data-protection document, or asks what such a document must contain — e.g. "draft a privacy policy", "fill in a DPIA", "review our processor agreement", "prepare an ICO breach notification". Cites UK GDPR articles, DPA 2018, and ICO guidance, as amended by the Data (Use and Access) Act 2025.
---

# UK GDPR Document Drafting (v2 — full templates)

The user wants help with: $ARGUMENTS (if empty, ask which document they need).

Read `${CLAUDE_PLUGIN_ROOT}/references/legal-framework.md` and `${CLAUDE_PLUGIN_ROOT}/references/duaa-2025-changes.md` before drafting, then start from the matching template:

| Document | Template | Authority |
|---|---|---|
| Privacy notice | `${CLAUDE_PLUGIN_ROOT}/templates/privacy-notice.md` | Arts 12–14 |
| RoPA (controller) | `${CLAUDE_PLUGIN_ROOT}/templates/ropa-controller.md` | Art 30(1) |
| RoPA (processor) | official ICO workbook: `${CLAUDE_PLUGIN_ROOT}/sources/ico-ropa-template-processor.xlsx` | Art 30(2) |
| DPIA | `${CLAUDE_PLUGIN_ROOT}/templates/dpia.md` (mirrors the ICO sample template; worked example in `sources/ico-dpia-example-completed.pdf`) | Art 35 |
| Processor agreement (DPA) | `${CLAUDE_PLUGIN_ROOT}/templates/processor-agreement.md` | Art 28(3) |
| LIA | `${CLAUDE_PLUGIN_ROOT}/templates/lia.md` | Art 6(1)(f) |
| Breach notification — ICO | `${CLAUDE_PLUGIN_ROOT}/templates/breach-notification-ico.md` | Art 33 |
| Breach notification — individuals | `${CLAUDE_PLUGIN_ROOT}/templates/breach-notification-individuals.md` | Art 34 |
| Transfer risk assessment (TRA) | `${CLAUDE_PLUGIN_ROOT}/templates/tra.md` — applies the DUAA "not materially lower" test | Art 46 (as amended by DUAA 2025) |
| International transfers | use the official instruments directly: `sources/ico-idta.pdf` (IDTA) / `sources/ico-addendum.pdf` (UK Addendum) — populate their tables; do not improvise transfer clauses | Art 46, DPA 2018 s.119A |

## Workflow

1. **Gather the facts.** Ask the user targeted questions to fill the template's placeholders: controller identity, purposes, data categories (flag special category/criminal offence data), recipients/processors, destinations outside the UK, retention, whether children are in scope. One focused round of questions; batch them.
2. **Instantiate the template.** Replace `{{placeholders}}` with the user's facts. **Never invent organisational facts** — retention periods, recipients, lawful bases and safeguards are the organisation's decisions; anything unknown stays as `[TO CONFIRM: …]`. Delete inapplicable sections and say which were dropped and why. Keep the bracketed article citations for the reviewer's benefit unless the user wants a clean copy.
3. **Check completeness.** Run the template's reviewer checklist and report each item as satisfied or outstanding.
4. **Close with the standing note** (below).

For **reviews of existing documents**: diff the user's document against the template and the cited articles; report gaps as a table (missing/deficient item → authority → suggested wording).

## Rules

- Cite the specific article/section beside each substantive section so a reviewing lawyer can verify quickly.
- UK law governs (UK GDPR + DPA 2018 as amended by DUAA 2025). Flag EU divergences where the user also operates there (ADM: EU Art 22 vs UK Arts 22A–22D; recognised legitimate interests is UK-only).
- Time-critical documents first: for a live breach, produce the Art 33 notification content before polishing anything else — the 72-hour clock is running.
- Consistency: facts must match across documents (what the privacy notice says must match the RoPA; what the ICO is told must match what individuals are told).

## Standing note (include with every produced document)

> This document was generated from the gdpr-uk plugin's templates and the facts you provided. It is a working draft, not legal advice: have your Data Protection Officer or legal counsel review it before adoption or publication, and resolve every `[TO CONFIRM]` marker first.
