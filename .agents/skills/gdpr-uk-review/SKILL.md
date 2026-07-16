---
name: gdpr-uk-review
description: Audit code, configurations, database schemas, APIs, and data flows for UK GDPR and data-protection compliance. Use for privacy reviews of personal-data handling, cookie and consent flows, retention, logging, rights support, automated decisions, processors, transfers, security, breach readiness, and ICO readiness. Produce evidence-based, severity-rated findings with precise UK GDPR, DPA 2018, DUAA 2025, PECR, and ICO citations. Do not use for document drafting or general legal Q&A.
---

# UK GDPR Compliance Review

Determine the review target from the current user request. If none is provided, review the current repository or ask the user to identify the target when scope is ambiguous.

## Read before analysing

Resolve paths relative to this skill directory.

- Read `../../../references/legal-framework.md` and `../../../references/duaa-2025-changes.md` for every review.
- Read `../../../references/exemptions.md` when exemptions, DSAR handling, or public-sector and law-enforcement contexts arise.
- Consult `../../../sources/SOURCES.md` and the matching primary instrument for article- or section-level questions. Verify current, high-stakes conclusions against official legislation.gov.uk or ico.org.uk sources.

## Methodology

Work through each relevant stage. Explicitly identify any skipped stage.

### 1. Identify personal data

Scan for information relating to identifiable living people, including contact details, online identifiers, cookies, location, account IDs, free text, images, and voice. Treat pseudonymised data, hashed emails, and joinable identifiers as personal data. Flag special-category data under Art 9 and criminal-offence data under Art 10 separately; check DPA 2018 s.10 and Schedule 1 conditions.

### 2. Map flows

For every category, identify collection, storage, internal and external transmission, third-party SDKs, analytics, telemetry, logs, backups, crash reporters, and transfers outside the UK.

### 3. Check obligations

| Check | Authority | Evidence to seek |
|---|---|---|
| Lawful basis per purpose | Art 6; Art 9(2) and Sch 1 for special category | Documented basis; Art 7-standard consent; LIA; recognised legitimate interests where applicable |
| Transparency | Arts 12-14 | Notice at collection points covering actual purposes, recipients, and retention |
| Minimisation | Art 5(1)(c) | Unused fields, broad responses, excessive analytics |
| Retention | Art 5(1)(e) | TTLs, deletion jobs, backup expiry, log retention |
| Security | Arts 5(1)(f), 32 | Encryption, access control, secret handling, logs and URLs, non-production data |
| Rights support | Arts 15-21 | Locate, export, rectify, erase, and propagate changes through caches, queues, backups, and processors |
| Automated decisions | Arts 22A-22D | Solely automated significant decisions, information, representations, human intervention, contestability |
| Processors and sharing | Art 28 | Art 28(3) terms and subprocessor flow-down |
| International transfers | Chapter V; DPA 2018 s.17A | Adequacy, UK Extension, IDTA, UK Addendum, or Art 49 derogation |
| Cookies and device access | PECR reg 6 as amended | Prior consent or a valid DUAA exemption with information and opt-out; marketing consent and soft opt-in |
| Breach readiness | Arts 33-34 | Detection, alerting, 72-hour notification capability, breach log |
| DPIA triggers | Art 35 | High-risk processing, monitoring, innovative technology, children, profiling, and special-category scale |
| Children | DPA 2018 s.9; Children's Code; DUAA Art 25 duty | Age assurance, age-appropriate design, and parental consent where applicable |

### 4. Report

Produce:

1. **Summary**: overall posture and the most serious issues.
2. **Data inventory**: categories found, clearly flagging special-category and criminal-offence data.
3. **Findings** table with `#`, severity, finding, evidence, authority, and remediation. Use file-and-line evidence when reviewing code.
4. **What could not be assessed**: contracts, policies, training, assessments, or other organisational evidence unavailable in the artefact.
5. **Disclaimer**: this is a technical compliance review, not legal advice; Critical and High findings should be reviewed by a DPO or legal counsel.

Use these severities:

- **Critical**: apparent unlawful processing or breach-level exposure.
- **High**: clear evidence of a material obligation gap.
- **Medium**: a gap likely to be non-compliant.
- **Low**: hardening or best practice.

## Rules

- Cite a specific provision for every finding; never cite only “GDPR.”
- Apply UK law as amended by DUAA 2025. Where EU law may also apply, flag material divergence and overlapping obligations.
- Treat absence of evidence as risk, not proof of breach.
- Keep the review read-only unless the user separately asks to implement remediations.
- Never invent provisions. Check the repository references or primary sources; if uncertainty remains, name the governing instrument and recommend verification.
