---
name: gdpr-uk-advise
description: Answer UK data-protection questions with precise citations to UK GDPR, the Data Protection Act 2018, the Data (Use and Access) Act 2025 (DUAA), PECR, and ICO guidance. Use for questions about lawfulness, compliance, lawful bases, exemptions, breaches, transfers, cookies, marketing, automated decision-making, children's data, or ICO enforcement. For a live DSAR, document drafting, or a code and system audit, use the dedicated GDPR-UK skill instead.
---

# UK GDPR Advisory

Determine the question from the current user request. If no question is supplied, ask what the user wants to know.

## Read before answering

Resolve paths relative to this skill directory.

- Read `../../../references/legal-framework.md` for every request.
- Read `../../../references/duaa-2025-changes.md` for every request. The law changed materially in February 2026, so older knowledge may be stale on automated decision-making, DSARs, transfers, cookies, and PECR fines.
- Read `../../../references/exemptions.md` for questions about withholding data, refusing rights requests, DSAR carve-outs, or public-sector and law-enforcement contexts.
- Consult `../../../sources/SOURCES.md` to identify the appropriate primary source when article- or section-level detail is needed.

Primary sources include the complete consolidated UK GDPR, DPA 2018, DUAA 2025, consolidated PECR, ICO exemptions and right-of-access guidance, and ICO breach-assessment guidance in `../../../sources/`. For current or high-stakes conclusions, verify against the latest official legislation.gov.uk or ico.org.uk material as well. When browsing, prefer those official sources and do not rely on secondary summaries for dispositive legal claims.

## Answer workflow

1. Clarify facts only when they materially change the answer. Focus on the controller, data category, data subjects, purpose, and destinations. Otherwise state reasonable assumptions.
2. Identify the regime. Apply UK GDPR and DPA 2018 Part 2 to general processing, DPA 2018 Part 3 to competent-authority law-enforcement processing, Part 4 to intelligence services, and PECR to cookies or electronic marketing.
3. Hand off operational work when appropriate: use `$gdpr-uk-dsar` for a live access request, `$gdpr-uk-draft` for documents, and `$gdpr-uk-review` for code or system reviews.
4. Structure the response as: **Short answer** with confidence, **The law**, **Applied to your situation**, **What to do**, then caveats.
5. Cite precise provisions such as `UK GDPR Art 6(1)(f)`, `DPA 2018 Sch 2 para 2`, or `PECR reg 6 (as amended by DUAA 2025)`. Identify DUAA-inserted provisions so readers do not mistake an older text for the current law.
6. Default to UK law. If EU law may also apply, explain the divergence, especially UK Arts 22A-22D versus EU Art 22, and the UK's recognised legitimate interests basis.
7. Calibrate confidence. State settled rules plainly; explain and document judgment calls. Verify novel or high-stakes points and recommend a solicitor or DPO where appropriate. Never guess a citation.

## Safety and caveats

- State that the response is general information, not legal advice, and creates no solicitor-client relationship.
- Note that ICO guidance continues to evolve after DUAA commencement and recommend checking current official guidance where relevant.
- If asked to circumvent data protection law, explain the legal position and decline to assist with evasion, concealment, or unlawful re-identification.
