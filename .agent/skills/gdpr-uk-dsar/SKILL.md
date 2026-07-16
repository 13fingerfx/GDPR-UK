---
name: gdpr-uk-dsar
description: Run an end-to-end UK subject access request workflow under UK GDPR Article 15, covering recognition, identity checks, clarification and clock pauses, reasonable and proportionate searches, exemptions, third-party redactions, response assembly, and lawful refusal. Use when Codex must handle a received SAR or DSAR, calculate its deadline, decide whether to charge or refuse, plan searches and redactions, or deal with third-party, parental, or former-employee requests.
---

# UK DSAR Response Workflow

Determine the situation from the current user message. If the stage and actions taken are unclear, ask promptly because the deadline may already be running.

## Read first

Resolve paths relative to this skill directory.

- Read `../../../references/legal-framework.md` and `../../../references/duaa-2025-changes.md`.
- For operational detail, consult `../../../sources/ico-right-of-access.pdf`.
- For exemptions, read `../../../references/exemptions.md`.

The bundled ICO right-of-access guidance predates DUAA commencement on 5 February 2026. Its operational detail remains useful, but cite the reasonable-and-proportionate search duty and the clarification clock pause to UK GDPR Art 15 as amended by DUAA 2025. Verify current high-stakes points against official sources.

## Stage 0: Triage on receipt

- Recognise requests made through any channel; no form, magic words, or GDPR reference is required.
- Log the received date. Day one is receipt; the deadline is the corresponding date in the following month, moving to the next working day if necessary.
- Route the request internally without delay.

## Stage 1: Validate the requester

- Verify identity only when there are reasonable doubts and request proportionate evidence promptly.
- For third-party requests, confirm authority such as written authorisation or power of attorney.
- Assess a child's competence rather than applying a fixed access age. DPA 2018 s.9's age of 13 concerns online consent, not access competence.
- UK GDPR covers living individuals; identify other regimes when deceased persons' records are involved.

## Stage 2: Scope, clarification, and fees

- Seek prompt, specific clarification only when genuinely needed to locate data. The clock pauses while awaiting a reasonably requested clarification, but the requester may decline to narrow scope.
- Charge nothing unless Art 12(5)'s manifestly unfounded or excessive threshold is met, or the requester seeks additional copies already supplied.
- Extend by up to two months only for complex or numerous requests, and notify the requester within the first month with reasons.
- Provide reasonable adjustments and accessible formats where needed.

## Stage 3: Search

- Plan and document a reasonable and proportionate search: systems, terms, custodians, and date ranges.
- Consider databases, CRM, email, messaging, HR, recordings, CCTV, access logs, backups, archives, and work data on personal devices or accounts.
- Exclude truly anonymised data and duplicate copies. Redact third-party data rather than treating whole documents as out of scope.
- Never delete data after receipt to avoid disclosure; DPA 2018 s.173 may apply.

## Stage 4: Withhold and redact

Apply exemptions per document, only to the extent necessary, and record the reasoning.

| Issue | Approach | Authority |
|---|---|---|
| Other people's data | Seek consent where appropriate; otherwise assess reasonableness and redact only third-party elements | DPA 2018 Sch 2 para 16 |
| Legal advice | Apply legal professional privilege where the test is met | Sch 2 para 19 |
| Crime prevention or investigation | Apply and document the prejudice test; never use a blanket exemption | Sch 2 para 2 |
| Health data | Apply the serious-harm test and obtain professional input where required | Sch 3 |
| Confidential references | Apply the specific confidential-reference exemption | Sch 2 para 24 |
| Ongoing negotiations | Withhold only the negotiating position while disclosure would prejudice it | Sch 2 para 22 |
| Management forecasting | Apply the prejudice-based and time-limited exemption | Sch 2 para 20 |
| Manifestly unfounded or excessive request | Apply the high Art 12(5) threshold and document defensible reasons | Art 12(5) |

## Stage 5: Respond

Deliver securely in a commonly used electronic form where appropriate:

1. A copy of personal data in intelligible form, with jargon explained and redactions marked.
2. Art 15(1)(a)-(h) information: purposes, categories, recipients, transfer safeguards, retention, rights, ICO complaint right, sources, and qualifying automated decision-making information under Arts 22A-22D.
3. A privacy-notice link only where it answers every required item for this person's data.

For a full or partial refusal, respond without undue delay and within one month. Explain the ground and reasoning unless that would undermine the exemption, and state the rights to complain internally, complain to the ICO, and seek a court order under DPA 2018 s.167.

## Stage 6: Close out

Record receipt, clarification, pause and response dates; the search plan; scope decisions; exemptions; withheld or redacted material; and delivery method.

## Output

For a live request, produce:

1. A deadline calculation including pauses.
2. A request-specific action list with owners.
3. A search plan.
4. An exemptions analysis.
5. A draft response-letter skeleton containing the Art 15(1) items.

Mark missing facts as `[TO CONFIRM]`. State that the output is not legal advice and that contested refusals should go to the DPO or legal counsel.
