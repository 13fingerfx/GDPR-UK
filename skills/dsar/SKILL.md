---
name: dsar
description: End-to-end workflow for handling a subject access request (SAR/DSAR) under UK GDPR Article 15 — recognising a request, verifying identity, clarifying scope and pausing the clock, running a reasonable and proportionate search, applying exemptions and third-party redactions, assembling the response, and refusing lawfully. Use when the user says they have received a subject access request or DSAR, asks how to respond to one, how long they have, whether they can refuse or charge, what to redact, or how to handle requests from third parties, parents, or ex-employees. Grounded in the ICO right-of-access guidance and UK GDPR as amended by the Data (Use and Access) Act 2025.
---

# DSAR Response Workflow

Situation: $ARGUMENTS (if empty, ask what stage the request is at and what's been done so far — the deadline may already be running).

**Read first**: `${CLAUDE_PLUGIN_ROOT}/references/legal-framework.md` and `${CLAUDE_PLUGIN_ROOT}/references/duaa-2025-changes.md`. For detailed operational questions, consult the ICO's Right of Access guidance directly: `${CLAUDE_PLUGIN_ROOT}/sources/ico-right-of-access.pdf` (v1.0.87, 8 Dec 2025, 124 pages). For exemptions: `${CLAUDE_PLUGIN_ROOT}/references/exemptions.md`.

> **Currency warning**: the ICO guidance in `sources/` predates DUAA commencement (5 Feb 2026). Its operational detail stands, but two points now have a **statutory** footing that the guidance describes only as practice: (1) the search duty is limited to a **reasonable and proportionate** search; (2) the response clock **pauses while you await clarification** you reasonably requested. Cite these to UK GDPR Art 15 as amended by DUAA 2025, not just to the guidance.

## Stage 0 — Triage (do this the day the request arrives)

- **Recognise it.** A SAR needs no form, no magic words, no mention of "GDPR" — any request by which someone asks for their personal data counts, made through any channel (email, letter, phone, social media, a complaint that includes "send me everything you hold on me"). You may invite use of a standard form but **cannot require it**.
- **Log the received date.** The one-month deadline runs from the day of receipt (day one is the day of receipt; the deadline is the corresponding date in the following month). Weekends/holidays: if the corresponding date is a non-working day, the deadline is the next working day.
- **Route it.** Anyone in the organisation might receive one — confirm staff who received it forwarded it immediately.

## Stage 1 — Validate the requester

- **Identity**: verify only if you have reasonable doubts, and ask only for what's proportionate — don't demand notarised ID from a logged-in account holder. The clock effectively starts when you receive the request; prompt ID requests protect you, late ones don't extend anything.
- **Third-party requests** (solicitor, relative, employer's HR on behalf of someone): satisfy yourself the third party is authorised (written authority, power of attorney). The data belongs to the data subject — respond to/via the authorised route.
- **Children**: a child with sufficient understanding exercises their own right; parents act for children who lack it. For online services remember the s.9 DPA 2018 age of 13 for consent contexts, but access turns on the child's competence, not a fixed age.
- **Deceased**: UK GDPR only covers living individuals — but the requester's own data mixed with a deceased person's may still be in scope, and other regimes (Access to Health Records Act 1990) may apply.

## Stage 2 — Scope, clarification, fees

- **Clarify** if you genuinely need it to find the data ("all my data" from a 10-year employee): ask promptly and specifically. **The clock pauses** from your clarification request until their reply [DUAA]. You cannot use clarification to whittle the request down — the requester may decline to narrow it and you must still do a reasonable and proportionate search of everything.
- **Fees**: none, unless the request is manifestly unfounded or excessive, where you may charge a reasonable admin fee **or** refuse (Art 12(5)). Additional copies of already-provided data: reasonable fee.
- **Extension**: +2 months for complex or numerous requests (Art 12(3)) — tell the requester within the first month with reasons. Volume alone doesn't make a request complex; ICO examples of complexity include technical difficulties in retrieval, special-category clinical data needing professional input, large volumes of third-party material.
- **Reasonable adjustments**: disabled requesters may need the response in accessible formats.

## Stage 3 — Search

- **Standard**: a **reasonable and proportionate** search [Art 15 as amended by DUAA 2025] — not a limitless one, but you must be able to justify where you didn't look. Document the search plan: systems queried, search terms, custodians, date ranges.
- **Scope includes**: live databases and CRM, email (including where the requester is discussed, not just addressed), messaging tools, HR systems, call recordings, CCTV, access logs, **backups and archived data** (in scope if retrievable — "it's in the archive" is not an exemption), and personal devices/accounts if used for work processing.
- **Out of scope**: truly anonymised data; other people's data (redact, Stage 4); repeated identical copies (one copy suffices); data deleted before the request arrived (deleting **after** receipt to avoid disclosure is a criminal offence — DPA 2018 s.173).
- **Unstructured manual records**: special, narrower rules for paper records outside a filing system (mainly public authorities — DPA 2018 ss.21, 24).

## Stage 4 — Withhold and redact (exemptions)

Apply per-document, to the minimum extent necessary; record every reliance. Most common in DSARs:

| Issue | Approach | Authority |
|---|---|---|
| Other people's data | Disclose if the third party consents or it's reasonable without consent (consider confidentiality, steps to seek consent, express refusal); otherwise redact the third-party elements, not the whole document | DPA 2018 Sch 2 para 16 |
| Legal advice | Legal professional privilege exemption | Sch 2 para 19 |
| Crime prevention/investigation | Prejudice test per request — never blanket | Sch 2 para 2 |
| Health data | Serious-harm test; obtain the appropriate health professional's opinion where required | Sch 3 |
| References | Confidential references exempt in both directions | Sch 2 para 24 |
| Ongoing negotiations with the requester | Only the record of your negotiating position, while disclosure would prejudice it | Sch 2 para 22 |
| Management forecasting (e.g. unannounced restructure) | Prejudice-based, time-limited | Sch 2 para 20 |
| **Manifestly unfounded/excessive** | High bar: "unfounded" means no genuine intent to exercise the right (e.g. offers to withdraw for payment, pure harassment); "excessive" is judged per request, and a repeat request isn't automatically excessive after time has passed. Refuse or charge — and be ready to defend it to the ICO | Art 12(5) |

## Stage 5 — Respond

Provide, in commonly used electronic form where the request was electronic (Art 15(3)), securely delivered:

1. **A copy of the personal data** — intelligible, with codes/jargon explained, redactions marked rather than silent.
2. **The Art 15(1)(a)–(h) supplementary information**: purposes; categories; recipients (or categories, incl. international recipients and safeguards); retention period or criteria; the rights of rectification, erasure, restriction and objection; the right to complain to the ICO; source of the data if not collected from them; existence of automated decision-making within Arts 22A–22D with meaningful information about logic, significance and consequences.
3. Much of this can be a link to the privacy notice **only if** the notice actually answers each item for this individual's data.

**If refusing** (wholly or partly): tell them without undue delay and within one month — which exemption/ground, why (unless explaining would undermine the exemption), their right to complain to you, then the ICO (statutory complaints route: acknowledge within 30 days [DUAA]), and to seek a court order (DPA 2018 s.167).

## Stage 6 — Close out

Record: dates (received, clarified, paused, responded), search plan and scope decisions, exemptions applied with reasoning, what was withheld/redacted, delivery method. This file is your defence in an ICO complaint (s.165) and evidences Art 5(2) accountability.

## Output

For a live request, produce: (1) a deadline calculation with any pause; (2) a stage-by-stage action list for THIS request with owners; (3) a search plan; (4) an exemptions analysis for any flagged material; (5) a draft response letter skeleton with the Art 15(1) items. Mark facts you weren't given as `[TO CONFIRM]`. Close with the standing note that this is not legal advice and contested refusals should go to the DPO or counsel.
