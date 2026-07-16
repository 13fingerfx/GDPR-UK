# UK Data Protection Legal Framework — Core Reference

> Current as of July 2026. The UK regime is the **UK GDPR** (retained EU Regulation 2016/679, as amended) read together with the **Data Protection Act 2018 (DPA 2018)**, both as amended by the **Data (Use and Access) Act 2025 (DUAA)** — Royal Assent 19 June 2025, with the majority of provisions in force from 5 February 2026 and phased commencement completing in June 2026. Where DUAA has changed the law, this reference states the amended position and flags the change. See `duaa-2025-changes.md` for a consolidated list of amendments.

## The instruments and how they fit together

| Instrument | Role |
|---|---|
| UK GDPR | Principal rules for general processing: principles, lawful bases, rights, obligations, transfers |
| DPA 2018 Part 2 | Supplements UK GDPR for general processing (conditions for special category data, exemptions via Schedules 2–4, children's consent age of 13 in s.9) |
| DPA 2018 Part 3 | Separate regime for **law enforcement processing** by competent authorities (ss.29–81) |
| DPA 2018 Part 4 | Separate regime for **intelligence services** processing (ss.82–113) |
| DPA 2018 Parts 5–6 | The Information Commissioner (Part 5) and enforcement powers (Part 6, ss.142–181) |
| PECR 2003 | Cookies, electronic marketing, network security (as amended by DUAA — see below) |
| DUAA 2025 | Amends all of the above; also creates smart-data schemes and digital verification services |

**Regulator**: the Information Commissioner's Office (ICO). DUAA ss.118–119 replace the Commissioner (a corporation sole) with a body corporate, the **Information Commission**, whose chair retains the title "Information Commissioner". Guidance and enforcement continuity are preserved.

## Key definitions (UK GDPR Art 4; DPA 2018 s.3)

- **Personal data**: any information relating to an identified or identifiable living individual ("data subject"). Identifiability includes indirect identification by reference to identifiers (name, ID number, location data, online identifier) or factors specific to identity. Pseudonymised data remains personal data; truly anonymised data does not.
- **Processing**: any operation on personal data — collection, recording, storage, adaptation, retrieval, disclosure, combination, erasure.
- **Controller**: determines the purposes and means of processing (Art 4(7)).
- **Processor**: processes on behalf of a controller (Art 4(8)). Joint controllers: Art 26.
- **Special category data** (Art 9(1)): racial/ethnic origin, political opinions, religious/philosophical beliefs, trade union membership, genetic data, biometric data (for identification), health data, sex life/sexual orientation.
- **Criminal offence data**: Art 10 / DPA 2018 s.10(4)–(5) — personal data relating to criminal convictions and offences or related security measures.

## The seven principles (UK GDPR Art 5)

1. **Lawfulness, fairness and transparency** — Art 5(1)(a)
2. **Purpose limitation** — Art 5(1)(b): collected for specified, explicit, legitimate purposes; not further processed incompatibly. DUAA inserted new Art 8A and Annex 2 clarifying when further processing is compatible.
3. **Data minimisation** — Art 5(1)(c): adequate, relevant, limited to what is necessary.
4. **Accuracy** — Art 5(1)(d): accurate and, where necessary, kept up to date.
5. **Storage limitation** — Art 5(1)(e): kept in identifiable form no longer than necessary.
6. **Integrity and confidentiality (security)** — Art 5(1)(f): appropriate technical and organisational measures.
7. **Accountability** — Art 5(2): the controller must be able to **demonstrate** compliance with all of the above.

## Lawful bases (UK GDPR Art 6)

Processing is lawful only if at least one applies, identified **before** processing begins and stated in the privacy notice:

| Basis | Article | Notes |
|---|---|---|
| Consent | 6(1)(a) | Art 7 conditions: freely given, specific, informed, unambiguous; as easy to withdraw as to give; not bundled. Children's online services: age 13 in the UK (DPA 2018 s.9) |
| Contract | 6(1)(b) | Necessary for a contract with the data subject or pre-contract steps at their request |
| Legal obligation | 6(1)(c) | UK legal obligation, not contractual |
| Vital interests | 6(1)(d) | Life-or-death situations |
| Public task | 6(1)(e) | Exercise of official authority or task in the public interest laid down by law (DPA 2018 s.8) |
| Legitimate interests | 6(1)(f) | Requires the three-part test: purpose, necessity, balancing (LIA). Not available to public authorities acting in performance of their tasks |
| **Recognised legitimate interests** | **6(1)(ea) — NEW (DUAA)** | Processing necessary for a purpose in new **Annex 1 UK GDPR**: national security/public security/defence; responding to emergencies; detecting/investigating/preventing crime; safeguarding vulnerable individuals; democratic engagement disclosures; disclosures to public bodies exercising public tasks who request the data. **No balancing test required** — but necessity must still be shown |

**Special category data** additionally requires an Art 9(2) condition, most of which are gated through **DPA 2018 s.10 and Schedule 1** (e.g. employment/social security (Sch 1 para 1), health/social care (para 2), public health (para 3), research (para 4), substantial public interest conditions (paras 6–28) — most substantial-public-interest conditions require an **Appropriate Policy Document** (Sch 1 Part 4)).

**Criminal offence data** requires official authority or a Schedule 1 condition (DPA 2018 s.10(5)).

## Transparency (Arts 12–14)

- **Art 13**: information to provide when data is collected **from the data subject** (at the time of collection).
- **Art 14**: information when data is obtained **from another source** (within one month, at first communication, or at first disclosure — whichever is earliest).
- **Art 12**: concise, transparent, intelligible, easily accessible, clear and plain language — especially for children.
- Required contents are listed in the drafting checklists (`skills/draft`).

## Data subject rights (Arts 15–22D)

| Right | Article | Time limit | Key points |
|---|---|---|---|
| Access (DSAR) | 15 | 1 month (extendable +2 for complex/numerous) | **DUAA change**: controller need only conduct a **reasonable and proportionate search**; the clock can be "stopped" while awaiting clarification from the requester. Fee only if manifestly unfounded/excessive; identity verification allowed |
| Rectification | 16 | 1 month | |
| Erasure | 17 | 1 month | Grounds in 17(1); exceptions in 17(3) (freedom of expression, legal obligation, public health, research, legal claims) |
| Restriction | 18 | 1 month | |
| Notification duty | 19 | — | Tell recipients of rectification/erasure/restriction |
| Portability | 20 | 1 month | Consent or contract basis + automated processing only; structured, commonly used, machine-readable format |
| Objection | 21 | 1 month | Absolute right to object to direct marketing; otherwise controller may continue with compelling legitimate grounds |
| Automated decision-making | **22A–22D (DUAA — Art 22 repealed)** | — | See below |

**Automated decision-making (DUAA rewrite — the largest UK/EU divergence).** Old Art 22 (general prohibition with exceptions) is repealed. New framework:
- **Art 22A** defines a "significant decision" (legal or similarly significant effect) and when a decision is "based solely on automated processing" (no **meaningful human involvement** — human involvement is not meaningful if merely token).
- **Art 22B**: significant decisions based entirely on automated processing are **permitted for ordinary personal data**, subject to safeguards; for **special category data** the old restrictive position is retained (broadly: explicit consent, contract necessity, or authorised by law with safeguards).
- **Art 22C** safeguards: provide information about the decision, enable representations, enable human intervention, enable contesting the decision.
- **Art 22D**: Secretary of State may make regulations clarifying the framework.
- Practical effect: pure-ADM using ordinary personal data no longer needs to fit an Art 22(2) exception, but the Art 22C safeguards are mandatory.

## Accountability obligations

- **Records of processing activities (RoPA)** — Art 30. Required contents in the drafting checklists. Exemption for organisations <250 employees unless processing is non-occasional, risky, or involves special category/criminal data (Art 30(5)) — in practice most organisations need one.
- **Data protection by design and by default** — Art 25.
- **Processor contracts** — Art 28(3): written contract with the mandatory clauses (see drafting checklists). Processors' own duties: Arts 28–33 (sub-processor flow-down, security, breach notification to controller without undue delay).
- **Security** — Art 32: appropriate measures including (as appropriate) pseudonymisation and encryption; confidentiality, integrity, availability and resilience; restoration; regular testing.
- **DPIA** — Art 35: required where processing is **likely to result in high risk**, and always for (a) systematic and extensive automated evaluation/profiling with significant effects, (b) large-scale processing of special category or criminal offence data, (c) systematic large-scale monitoring of publicly accessible areas. The ICO also lists operations requiring a DPIA (e.g. innovative technology, denial of service on the basis of profiling, large-scale biometrics/genetics, invisible processing, tracking, targeting children). Prior consultation with the ICO if residual risk is high (Art 36).
- **Data Protection Officer** — Arts 37–39: mandatory for public authorities, or where core activities involve regular and systematic large-scale monitoring, or large-scale special category/criminal data processing. DUAA did **not** abolish the UK DPO requirement.
- **UK representative** (Art 27): controllers/processors outside the UK offering goods/services to or monitoring people in the UK must appoint one (unless occasional, low-risk).

## Personal data breaches (Arts 33–34)

- **Breach**: a breach of security leading to accidental or unlawful destruction, loss, alteration, unauthorised disclosure of, or access to, personal data.
- **Art 33**: notify the **ICO without undue delay and where feasible within 72 hours** of becoming aware, unless the breach is *unlikely to result in a risk* to individuals. Phased notification allowed with reasons for delay. Document **all** breaches internally (Art 33(5)) — even unreported ones.
- **Art 34**: notify **affected data subjects without undue delay** where the breach is likely to result in a **high risk** — unless encryption/measures render data unintelligible, subsequent measures remove the high risk, or individual notice would be disproportionate (public communication instead).
- Processors: notify their controller without undue delay (Art 33(2)).
- Law-enforcement regime equivalents: DPA 2018 ss.67–68.

## International transfers (UK GDPR Ch V, as amended by DUAA)

- Transfers of personal data outside the UK require: **adequacy regulations** (DPA 2018 s.17A "data bridges" — includes the EEA and the UK Extension to the EU–US Data Privacy Framework), or **appropriate safeguards** (Art 46: the ICO's **International Data Transfer Agreement (IDTA)** or the **UK Addendum** to the EU SCCs, plus BCRs), or an Art 49 derogation (explicit consent, contract necessity, etc. — for occasional transfers).
- **DUAA change — the "data protection test"**: adequacy and safeguard assessments now ask whether the destination's standard of protection is **"not materially lower"** than the UK's, judged with regard to outcomes rather than a line-by-line equivalence exercise. Transfer risk assessments for Art 46 tools apply the same standard.
- A transfer to a country with no adequacy and no safeguards, without a derogation, is unlawful.

## PECR — cookies and electronic marketing (as amended by DUAA)

Full consolidated text (point-in-time 16 July 2026): `sources/pecr-2003-consolidated-2026-07-16.pdf`.

- **Structure since 5 Feb 2026**: regulation 6 was **substituted** by DUAA s.112(2) as a general prohibition on storing or accessing information in terminal equipment (expressly including instigating storage/access and collecting/monitoring information automatically emitted by the device), **subject to the exceptions in new Schedule A1** (inserted by DUAA Sch 12). Cite "PECR reg 6 and Sch A1 (as substituted/inserted by DUAA 2025)".
- **Schedule A1 exceptions** include: consent after clear and comprehensive information (para 2 — consent may be signified via browser or application settings); transmission of a communication (para 3); strictly necessary for a requested service (para 4); and the new **low-risk purposes** — statistical/analytics purposes to improve the service, appearance/functionality preferences, software security updates, and emergency assistance — subject to clear information and a right to object/opt-out. New reg 6A lets the Secretary of State amend the exceptions by regulations.
- Direct electronic marketing requires consent, or the "soft opt-in" for existing customers (DUAA extends the soft opt-in to **charities**).
- **DUAA raised PECR fines** from £500,000 to UK GDPR levels: up to **£17.5m or 4% of global annual turnover**.

## Exemptions (DPA 2018 Schedules 2–4)

Exemptions disapply specific rights/obligations to the minimum extent necessary, mostly subject to a **prejudice test** (applying the provision "would be likely to prejudice" the protected purpose). Applied case-by-case, never blanket. Headline categories (see `exemptions.md` for the full treatment):

- Crime and taxation (Sch 2 para 2); immigration (para 4); disclosure required by law / legal proceedings (para 5); legal professional privilege (para 19); parliamentary privilege, judicial appointments, Crown honours; regulatory functions (paras 7–11); journalism, academia, art, literature ("special purposes", para 26); research and statistics (para 27); archiving in the public interest (para 28); management forecasts (para 20); corporate finance (para 21); negotiations (para 22); confidential references (para 24); exam scripts and marks (para 25); health, social work and education data (Schedule 3); child abuse data (Schedule 3 Part 4); national security and defence (DPA 2018 ss.26–28, with ministerial certificates).

## Enforcement and penalties (DPA 2018 Part 6)

- ICO powers: information notices (s.142), assessment notices (s.146), enforcement notices (s.149), penalty notices (s.155).
- **Maximum fines** (s.157): **higher maximum** £17.5m or 4% of total worldwide annual turnover (whichever higher) — for breaches of principles, rights, transfer rules; **standard maximum** £8.7m or 2% — for breaches of controller/processor obligations (records, security, DPO, breach notification).
- Criminal offences: unlawfully obtaining personal data (s.170), re-identification of de-identified data (s.171), alteration of records to prevent disclosure after a DSAR (s.173).
- Individuals: compensation for material and **non-material** damage (Art 82 / DPA 2018 ss.168–169); complaints to the ICO (s.165).
- **DUAA statutory complaints process**: data subjects should complain to the **controller first**; controllers must acknowledge within **30 days** and respond without undue delay; the ICO may decline to act where the controller process hasn't been used.

## Children

- Consent age for online services ("information society services"): **13** in the UK (DPA 2018 s.9).
- ICO **Age Appropriate Design Code** (Children's Code): 15 standards for online services likely to be accessed by children — mandatory to take into account; enforced through UK GDPR.
- **DUAA**: new duty to take account of children's higher protection needs when designing services (amendments to Art 25 considerations for information society services).

## Disclaimer

This reference summarises the law for engineering and operational compliance work. It is not legal advice. For contested, novel, or high-stakes questions, consult a qualified solicitor or your Data Protection Officer. Verify currency against legislation.gov.uk and ico.org.uk — the DUAA commencement timetable ran to June 2026 and ICO guidance continues to be updated.
