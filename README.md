# GDPR-UK — UK Data Protection Compliance Plugin for Claude Code

A Claude Code plugin for working with **UK GDPR**, the **Data Protection Act 2018**, and the **Data (Use and Access) Act 2025 (DUAA)**. It reviews code and data flows for compliance gaps, guides the drafting of privacy documents, and answers UK data protection questions — always with precise citations (UK GDPR articles, DPA 2018 sections and Schedules, PECR regulations, ICO guidance) suitable to hand to a DPO or legal counsel.

> ## ⚠️ Scope — please read before adopting
>
> This plugin includes full document templates (privacy notice, RoPA, DPIA, Art 28 processor agreement, LIA, transfer risk assessment, and Art 33/34 breach notifications) in `templates/`, an end-to-end DSAR response workflow, and official ICO instruments in `sources/` (IDTA, UK Addendum, ICO DPIA and RoPA templates). Outputs are **working drafts**: they must be reviewed by your Data Protection Officer or legal counsel before adoption or publication, and any third party using or redistributing this plugin should make that clear to their own users.
>
> Nothing produced by this plugin is legal advice, and no solicitor–client relationship arises from its use.

## What's included

| Skill | Command | Auto-invokes when you… |
|---|---|---|
| **Compliance review** | `/gdpr-uk:review` | ask to review/audit code, schemas, APIs, configs, or data flows for GDPR or privacy compliance |
| **Document drafting** | `/gdpr-uk:draft` | ask to draft or review a privacy notice, RoPA, DPIA, processor agreement (DPA), LIA, or breach notification — instantiates the full templates in `templates/` from your facts |
| **Advisory Q&A** | `/gdpr-uk:advise` | ask whether something is lawful, how to handle a breach, which lawful basis or exemption applies, transfer/cookie/marketing rules, etc. |
| **DSAR workflow** | `/gdpr-uk:dsar` | say you've received a subject access request — runs the full response workflow: deadline calculation, identity checks, clarification and clock-pause, search plan, exemptions/redactions, response assembly, lawful refusal |

All four skills also trigger automatically from natural requests — the slash commands are optional.

### Reference library

The skills are grounded in a distilled reference library (`references/`) covering the current law **as amended by DUAA 2025** (in force from 5 February 2026), including:

- The seven principles, lawful bases (including the new **recognised legitimate interests** basis, Art 6(1)(ea)), special category and criminal offence data conditions (DPA 2018 s.10 + Schedule 1)
- Data subject rights, including the DUAA "reasonable and proportionate search" standard for DSARs and the rewritten automated decision-making framework (**Arts 22A–22D**, replacing Art 22)
- Accountability: RoPA, DPIAs, DPOs, processor contracts (Art 28), security (Art 32)
- Breach notification (Arts 33–34), international transfers (IDTA, UK Addendum, and the DUAA "data protection test"), PECR cookies and marketing (including the DUAA low-risk cookie exemptions and raised fines)
- The full DPA 2018 **Schedule 2–4 exemptions** with their prejudice tests, plus the Part 3 law-enforcement and Part 4 intelligence-services regimes
- Enforcement, penalties, and the DUAA statutory complaints process

### Primary sources (`sources/`)

Verified source documents ship with the plugin — see `sources/SOURCES.md` for the full manifest and verified coverage of each file. Highlights: the **complete UK GDPR consolidated text** (point-in-time 5 Feb 2026 — all 99 Articles and Annexes 1–2, including the DUAA-inserted provisions); the complete **DPA 2018** and **DUAA 2025** as enacted; **PECR fully consolidated to 16 July 2026**; ICO detailed guidance on **right of access** (Dec 2025) and **breach assessment**; the ICO **high-risk (DPIA) list** and **exemptions guide**; and the official **IDTA**, **UK Addendum**, **ICO DPIA template** and **processor RoPA workbook**. The skills consult these directly for article/section-level detail.

## Installation

This repository is itself a Claude Code plugin marketplace. To install for your user account (available across all your projects on that machine):

```bash
claude plugin marketplace add 13fingerfx/GDPR-UK
claude plugin install gdpr-uk@gdpr-uk-marketplace
```

Or from inside a Claude Code session: `/plugin marketplace add 13fingerfx/GDPR-UK`, then `/plugin install gdpr-uk`. Update later with `claude plugin update gdpr-uk`.

For one-off local development/testing:

```bash
git clone https://github.com/13fingerfx/GDPR-UK.git
claude --plugin-dir ./GDPR-UK
```

After changing plugin files mid-session, run `/reload-plugins` inside Claude Code.

### Codex

Codex discovers the repository-scoped ports from `.agents/skills/` when you work inside this checkout. Invoke them explicitly with `$gdpr-uk-review`, `$gdpr-uk-draft`, `$gdpr-uk-advise`, or `$gdpr-uk-dsar`; Codex can also select them automatically from a matching request.

The Codex skills reuse the same `references/`, `templates/`, and `sources/` content as the Claude Code plugin. Clone the repository and start Codex anywhere inside the checkout; no separate copy of those shared resources is required.

The repository is also a Codex plugin, described by `.codex-plugin/plugin.json`. Installing the plugin makes the complete skill suite and its shared resources persistently available beyond this checkout.

## Usage examples

```
/gdpr-uk:review src/api/users/
Can you audit this service for GDPR issues before we ship?

/gdpr-uk:draft privacy notice for a B2C fitness app
What does an Art 28 processor agreement have to contain?

/gdpr-uk:advise do we need consent for first-party analytics cookies?

/gdpr-uk:dsar we received a SAR from an ex-employee on 3 July — what now?
Can we refuse this subject access request as excessive?
```

## Currency

The reference material is current as of **July 2026** and reflects the DUAA 2025 amendments. Data protection law and ICO guidance continue to evolve — verify high-stakes points against [legislation.gov.uk](https://www.legislation.gov.uk) and [ico.org.uk](https://ico.org.uk).

## Roadmap

- ~~v2: full document templates~~ — **shipped** (`templates/`).
- ~~v3: DSAR response workflow + transfer risk assessment (TRA) helper~~ — **shipped** (`skills/dsar/`, `templates/tra.md`).
- Next candidate: Children's Code conformance checks — parked until the Code itself (15 standards) is sourced.
- Source gaps to fill (see `sources/SOURCES.md` § Wanted): ICO general DPIA guidance, the Children's Code itself, ICO controller RoPA template. The legislative backbone (UK GDPR, DPA 2018, DUAA 2025, PECR) is complete.

## License

MIT
