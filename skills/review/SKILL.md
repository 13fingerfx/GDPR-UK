---
name: review
description: UK GDPR compliance review of code, configurations, database schemas, APIs, and data flows. Use when the user asks to review, audit, or check code or a system for GDPR/data-protection compliance, privacy issues, personal data handling, or ICO-readiness — e.g. "review this service for GDPR", "audit our data flows", "is this schema compliant", "check our cookie banner / consent flow / retention logic / logging for personal data". Produces findings with severity ratings and citations to UK GDPR articles, DPA 2018 sections, and ICO guidance, as amended by the Data (Use and Access) Act 2025.
---

# UK GDPR Compliance Review

You are performing a UK data protection compliance review of code, configuration, schemas, or described data flows. Target of review: $ARGUMENTS (if empty, ask the user what to review, or review the current repository).

**Before analysing**, read the reference files for the current legal position:
- `${CLAUDE_PLUGIN_ROOT}/references/legal-framework.md` — always
- `${CLAUDE_PLUGIN_ROOT}/references/duaa-2025-changes.md` — always (the law changed materially in Feb 2026)
- `${CLAUDE_PLUGIN_ROOT}/references/exemptions.md` — when exemptions, DSAR handling, or public-sector/law-enforcement contexts arise

## Methodology

Work through these stages. Skip stages irrelevant to the artefact under review, but say so explicitly.

### 1. Identify personal data
Scan for anything relating to an identifiable living individual: names, emails, phone numbers, addresses, IP addresses, device/advertising IDs, cookies, location data, account IDs joinable to identity, free-text fields likely to contain personal data, photos, voice. Flag **special category data** (health, biometrics for identification, ethnicity, sexuality, religion, politics, trade-union, genetic — Art 9) and **criminal offence data** (Art 10) separately — these carry extra conditions (DPA 2018 s.10 + Schedule 1). Remember: pseudonymised data is still personal data; hashed emails and user IDs count.

### 2. Map the flows
For each category: where is it collected, where stored, where sent (internal services, third-party APIs, SDKs, analytics, logs, backups, crash reporters), and where does it leave the UK? Third-party SDKs and telemetry are the most commonly missed flows.

### 3. Check against obligations

| Check | Authority | What to look for |
|---|---|---|
| Lawful basis identifiable per purpose | Art 6; Art 9(2)+Sch 1 for special category | Is there a plausible documented basis? Consent implemented to Art 7 standard (granular, withdrawable, not pre-ticked)? Legitimate interests → is an LIA plausible? New recognised-legitimate-interests basis (Art 6(1)(ea), DUAA) where applicable |
| Transparency | Arts 12–14 | Privacy notice exists, is linked at collection points, covers all purposes/recipients/retention actually found in the code |
| Minimisation | Art 5(1)(c) | Fields collected but never used; over-broad API responses; "collect everything" analytics |
| Retention | Art 5(1)(e) | TTLs, deletion jobs, backup expiry; indefinite storage is a finding. Logs containing personal data need retention limits too |
| Security | Art 5(1)(f), Art 32 | Encryption in transit and at rest, access control, secrets handling, personal data in logs/error messages/URLs, test/staging environments using production data |
| Data subject rights support | Arts 15–21 | Can the system actually locate, export (portable format), rectify, and erase a person's data — including in caches, queues, backups, and third parties? DSAR search must be feasible (reasonable and proportionate, DUAA) |
| Automated decision-making | Arts 22A–22D (DUAA) | Solely-automated significant decisions: are the Art 22C safeguards implemented (information, representations, human intervention, contestability)? Special category data in ADM → restricted regime |
| Processors and sharing | Art 28 | Third-party services processing personal data → is there a DPA with Art 28(3) clauses? Sub-processor flow-down? |
| International transfers | Ch V; DPA 2018 s.17A | Non-UK hosting/APIs/support access: adequacy ("data bridge"), IDTA/UK Addendum, or Art 49 derogation? US services: is the vendor on the UK Extension to the Data Privacy Framework? |
| Cookies / device access | PECR reg 6 (as amended by DUAA) | Consent before non-essential storage/access; DUAA exemptions for first-party analytics, appearance, security — with information and opt-out. Marketing consent / soft opt-in |
| Breach readiness | Arts 33–34 | Detection/alerting exists; 72-hour ICO notification is operationally feasible; internal breach log |
| DPIA triggers | Art 35 | Large-scale special category data, systematic monitoring, innovative tech, children, profiling with significant effects → flag that a DPIA is required |
| Children | DPA 2018 s.9; ICO Children's Code; DUAA Art 25 duty | Age gating, age-appropriate design, parental consent under 13 |

### 4. Report

Output a findings report:

1. **Summary** — one paragraph: overall posture and the most serious issues.
2. **Data inventory** — table of personal data categories found, with special category/criminal data flagged.
3. **Findings** — table: `#`, Severity (**Critical** = unlawful processing or breach-level exposure / **High** = clear breach of an obligation / **Medium** = gap likely to be non-compliant / **Low** = hardening or best practice), Finding, Evidence (`file:line` where reviewing code), Authority (specific article/section), Remediation (concrete, actionable).
4. **What we could not assess** — organisational matters invisible in code (whether an LIA/DPIA/RoPA exists, contracts, training). Never assume these exist or don't.
5. **Disclaimer** — this is a technical compliance review, not legal advice; recommend findings rated Critical/High are shown to the organisation's DPO or legal counsel.

## Rules

- Cite the **specific** provision for every finding (e.g. "Art 32(1)(a) UK GDPR", "DPA 2018 s.170", "PECR reg 6 as amended by DUAA 2025") — never just "GDPR".
- Apply **UK** law: UK GDPR as amended by DUAA, not EU GDPR. Where the user also serves EU users, flag divergences (especially ADM: EU Art 22 vs UK Arts 22A–22D) and note the stricter rule governs.
- Absence of evidence is a finding of *risk*, not a finding of *breach* — phrase accordingly.
- Do not invent article numbers. If unsure of the exact provision, check the reference files; if still unsure, say which instrument governs and recommend verification.
