# GDPR-UK — UK Data Protection Compliance Plugin for Claude Code

A Claude Code plugin for working with **UK GDPR**, the **Data Protection Act 2018**, and the **Data (Use and Access) Act 2025 (DUAA)**. It reviews code and data flows for compliance gaps, guides the drafting of privacy documents, and answers UK data protection questions — always with precise citations (UK GDPR articles, DPA 2018 sections and Schedules, PECR regulations, ICO guidance) suitable to hand to a DPO or legal counsel.

> ## ⚠️ Version 1 scope — please read before adopting
>
> **This release (v1) provides structured guidance and completeness checklists — not finished legal templates.** The `draft` skill will help you build privacy notices, RoPAs, DPIAs, processor agreements, LIAs, and breach notifications by walking mandatory contents item-by-item, but its outputs are **working drafts** that must be reviewed by your Data Protection Officer or legal counsel before adoption or publication.
>
> Any third party using or redistributing this plugin should make this limitation clear to their own users. **Full document templates are planned for v2**, which is intended to follow swiftly.
>
> Nothing produced by this plugin is legal advice, and no solicitor–client relationship arises from its use.

## What's included

| Skill | Command | Auto-invokes when you… |
|---|---|---|
| **Compliance review** | `/gdpr-uk:review` | ask to review/audit code, schemas, APIs, configs, or data flows for GDPR or privacy compliance |
| **Document guidance** | `/gdpr-uk:draft` | ask to draft or review a privacy notice, RoPA, DPIA, processor agreement (DPA), LIA, or breach notification |
| **Advisory Q&A** | `/gdpr-uk:advise` | ask whether something is lawful, how to handle a DSAR or breach, which lawful basis or exemption applies, transfer/cookie/marketing rules, etc. |

All three skills also trigger automatically from natural requests — the slash commands are optional.

### Reference library

The skills are grounded in a distilled reference library (`references/`) covering the current law **as amended by DUAA 2025** (in force from 5 February 2026), including:

- The seven principles, lawful bases (including the new **recognised legitimate interests** basis, Art 6(1)(ea)), special category and criminal offence data conditions (DPA 2018 s.10 + Schedule 1)
- Data subject rights, including the DUAA "reasonable and proportionate search" standard for DSARs and the rewritten automated decision-making framework (**Arts 22A–22D**, replacing Art 22)
- Accountability: RoPA, DPIAs, DPOs, processor contracts (Art 28), security (Art 32)
- Breach notification (Arts 33–34), international transfers (IDTA, UK Addendum, and the DUAA "data protection test"), PECR cookies and marketing (including the DUAA low-risk cookie exemptions and raised fines)
- The full DPA 2018 **Schedule 2–4 exemptions** with their prejudice tests, plus the Part 3 law-enforcement and Part 4 intelligence-services regimes
- Enforcement, penalties, and the DUAA statutory complaints process

Primary sources are included in this repository: the full **Data Protection Act 2018** (`data-protection-act-2018.pdf`), the **ICO Guide to Data Protection Exemptions** (`ico-guide-to-data-protection-exemptions.pdf`), and the **GOV.UK UK GDPR overview** (`uk-gdpr-from-govuk.pdf`). The skills consult the Act directly for section-level detail.

## Installation

From a local clone:

```bash
git clone https://github.com/13fingerfx/gdpr-uk.git
claude --plugin-dir ./gdpr-uk
```

Or add this repository as a marketplace source and install the `gdpr-uk` plugin from it. After changes, run `/reload-plugins` inside Claude Code.

## Usage examples

```
/gdpr-uk:review src/api/users/
Can you audit this service for GDPR issues before we ship?

/gdpr-uk:draft privacy notice for a B2C fitness app
What does an Art 28 processor agreement have to contain?

/gdpr-uk:advise do we need consent for first-party analytics cookies?
How long do we have to answer a subject access request?
```

## Currency

The reference material is current as of **July 2026** and reflects the DUAA 2025 amendments. Data protection law and ICO guidance continue to evolve — verify high-stakes points against [legislation.gov.uk](https://www.legislation.gov.uk) and [ico.org.uk](https://ico.org.uk).

## Roadmap

- **v2 (next)**: full document templates — privacy notice, RoPA, DPIA, Art 28 processor agreement, LIA, and Art 33/34 breach notification letters — replacing the v1 checklist-guided drafting flow.
- Candidate later additions: DSAR response workflow, transfer risk assessment (TRA) helper, Children's Code conformance checks.

## License

MIT
