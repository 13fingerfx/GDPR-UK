---
name: draft
description: Guidance and checklists for UK GDPR compliance documents — privacy notices, records of processing activities (RoPA), data processing agreements (DPAs), data protection impact assessments (DPIAs), legitimate interests assessments (LIAs), and personal data breach notifications. Use when the user asks to draft, write, create, review, or check any privacy/data-protection document, or asks what such a document must contain — e.g. "draft a privacy policy", "what goes in a DPIA", "review our processor agreement", "prepare an ICO breach notification". Cites UK GDPR articles, DPA 2018, and ICO guidance, as amended by the Data (Use and Access) Act 2025.
---

# UK GDPR Document Guidance & Checklists

> **Version 1 scope — notice to all users, including third parties adopting this plugin:** this release provides **structured guidance and completeness checklists**, not finished legal templates. Outputs built from these checklists are working drafts that must be reviewed by your Data Protection Officer or legal counsel before adoption or publication. **Full document templates are planned for v2.** State this scope note when producing any document under this skill.

The user wants help with: $ARGUMENTS (if empty, ask which document they need). Read `${CLAUDE_PLUGIN_ROOT}/references/legal-framework.md` and `${CLAUDE_PLUGIN_ROOT}/references/duaa-2025-changes.md` before drafting.

**Approach for every document**: (1) gather the facts by asking the user targeted questions from the relevant checklist below; (2) produce a structured draft covering every mandatory item, marking anything unknown as `[TO CONFIRM: …]` rather than inventing facts; (3) append the checklist with each item ticked or flagged; (4) include the v1 scope note and the review-by-DPO/counsel recommendation.

## Privacy notice — Arts 13/14 UK GDPR

Mandatory contents (Art 13 — data collected from the individual; Art 14 adds source information):

- [ ] Controller identity and contact details (and UK representative, if Art 27 applies)
- [ ] DPO contact details, where one is appointed (Arts 37–39)
- [ ] **Each purpose** of processing and the **lawful basis for each** (Art 6; if legitimate interests — state the interests; if recognised legitimate interests (Art 6(1)(ea), DUAA) — state the Annex 1 purpose)
- [ ] Special category data: the Art 9(2) condition and DPA 2018 Sch 1 condition relied on
- [ ] Recipients or categories of recipients (name key processors/third parties)
- [ ] International transfers: destinations, mechanism (adequacy/data bridge, IDTA, UK Addendum), and how to obtain a copy of safeguards
- [ ] **Retention periods** per category (or the criteria used to determine them — real criteria, not "as long as necessary")
- [ ] Data subject rights (Arts 15–21), including the absolute right to object to direct marketing
- [ ] Right to withdraw consent, where consent is a basis (Art 7(3))
- [ ] Right to complain: **first to the controller** (DUAA statutory complaints process — provide the route and note the 30-day acknowledgment), then to the ICO (ico.org.uk)
- [ ] Whether provision is statutory/contractual and consequences of not providing
- [ ] Automated decision-making: existence, meaningful logic, significance and consequences; the Art 22C safeguards (information, representations, human intervention, contestability — DUAA)
- [ ] Art 14 only: categories of data and the source(s), including whether publicly accessible
- [ ] Timing: Art 13 — at collection; Art 14 — within one month / first communication / first disclosure, whichever is earliest
- [ ] Style: Art 12 — concise, plain language; layered notices and child-appropriate wording where relevant (ICO Children's Code)

## Record of processing activities (RoPA) — Art 30

Controller records (Art 30(1)): name/contacts of controller (and joint controllers, representative, DPO); purposes; categories of data subjects and personal data; categories of recipients; international transfers and safeguards; retention periods where possible; general description of Art 32 security measures. Processor records (Art 30(2)): processor and each controller served; categories of processing; transfers; security measures. The Art 30(5) small-organisation exemption rarely applies in practice (any non-occasional processing loses it). Recommend one row per processing activity, owned and dated.

## Data processing agreement (processor contract) — Art 28(3)

Every clause below is **mandatory**; a missing clause is a compliance gap for both parties:

- [ ] Subject matter, duration, nature and purpose of processing; types of personal data; categories of data subjects; controller's obligations and rights (Art 28(3) chapeau)
- [ ] Process only on the controller's **documented instructions**, including for transfers (28(3)(a))
- [ ] Confidentiality commitments for authorised persons (28(3)(b))
- [ ] Art 32 security measures (28(3)(c))
- [ ] Sub-processors: prior specific or general written authorisation, flow-down of the same obligations, processor remains fully liable (28(2), 28(4))
- [ ] Assist the controller with data subject rights requests (28(3)(e))
- [ ] Assist with security, **breach notification (without undue delay to the controller)**, DPIAs and prior consultation (28(3)(f), 33(2))
- [ ] Delete or return all personal data at end of services (28(3)(g))
- [ ] Audits and inspections; inform controller if an instruction infringes data protection law (28(3)(h))
- [ ] Transfers annex where processing leaves the UK (IDTA / UK Addendum incorporated)

## DPIA — Art 35

Required where processing is likely to result in **high risk**, and always for: systematic extensive profiling with significant effects; large-scale special category/criminal data; large-scale systematic monitoring of public areas (Art 35(3)); plus the ICO's list (innovative technology, invisible processing, large-scale biometrics/genetics, tracking, targeting children, denial of service from profiling). Minimum contents (Art 35(7)):

- [ ] Systematic description of the processing and purposes (include a data-flow description; legitimate interests if relied on)
- [ ] Necessity and proportionality assessment (lawful basis; could the purpose be achieved with less data?)
- [ ] Assessment of risks to individuals' rights and freedoms (likelihood × severity; consider ADM under Arts 22A–22D, children, vulnerable groups)
- [ ] Measures to address the risks and demonstrate compliance
- [ ] DPO advice sought and recorded (Art 35(2)); data subjects' views where appropriate (35(9))
- [ ] Outcome: if residual risk remains **high**, prior consultation with the ICO is mandatory before processing (Art 36)

## Legitimate interests assessment (LIA) — Art 6(1)(f)

Three-part test, documented: **Purpose** (what interest? whose? is it legitimate?), **Necessity** (does the processing achieve it? less intrusive alternative?), **Balancing** (nature of data, reasonable expectations, impact, safeguards, opt-out). Not needed for the DUAA recognised-legitimate-interests basis (Art 6(1)(ea)) — but record which Annex 1 purpose applies and why the processing is necessary for it.

## Personal data breach — Arts 33/34

**To the ICO** (Art 33 — without undue delay, within 72 hours of awareness where feasible; reasons for any delay; phased notification allowed). Contents (Art 33(3)):

- [ ] Nature of the breach: categories and approximate numbers of data subjects and records
- [ ] DPO/contact point
- [ ] Likely consequences
- [ ] Measures taken or proposed, including mitigation
- [ ] If not notifying: documented reasoning why the breach is *unlikely to result in a risk* — and log it internally regardless (Art 33(5))

**To individuals** (Art 34 — where likely **high risk**): plain-language description, DPO contact, likely consequences, measures taken; exceptions where data was unintelligible (e.g. encrypted with keys uncompromised), subsequent measures removed the high risk, or disproportionate effort (public communication instead). Processors notify their controller without undue delay (Art 33(2)).

## Rules

- Ask before inventing: retention periods, recipients, and lawful bases are facts about the organisation — get them from the user or mark `[TO CONFIRM]`.
- Cite the specific article/section beside each section of the draft so a reviewing lawyer can verify quickly.
- UK law governs (UK GDPR + DPA 2018 as amended by DUAA 2025). Flag EU-facing divergences where the user operates in both markets.
- Always close with: the v1 guidance-and-checklist scope note, and a recommendation for DPO/legal review before adoption.
