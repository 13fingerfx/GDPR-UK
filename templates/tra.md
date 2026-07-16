# Transfer Risk Assessment (TRA) — Template (UK GDPR Art 46, as amended by DUAA 2025)

> Required when you rely on an **Art 46 transfer tool** (IDTA or UK Addendum — `sources/ico-idta.pdf`, `sources/ico-addendum.pdf`) for a restricted transfer. Not needed where UK **adequacy regulations** ("data bridge", DPA 2018 s.17A) cover the destination — check the current list on gov.uk — or where you properly rely on an **Art 49 derogation** (occasional transfers only; document the derogation instead).
>
> **The test** [DUAA 2025]: would the standard of protection for the data subjects, after the transfer and with the transfer tool in place, be **"not materially lower"** than under UK law? This is an **outcome-focused** judgment, not a line-by-line comparison of foreign law with the UK GDPR. The ICO's TRA tool takes a comparable risk-based approach; this template follows the same logic under the current statutory standard.

| Document control | |
|---|---|
| Transfer / arrangement assessed | {{…}} |
| Exporter / importer | {{controller or processor role of each}} |
| Author / date / review date | {{…}} — review on renewal, scope change, or material change in the destination |
| DPO consulted | {{Y/N, date}} |

## Step 1 — Describe the transfer

- Personal data categories transferred: {{…; flag special category / criminal offence / children's data}}
- Data subjects: {{…}} and approximate volume: {{…}}
- Purpose of the transfer: {{…}}
- Destination country/countries and importer: {{…; include onward-transfer destinations and the importer's sub-processors}}
- Format and access: {{transferred and stored / remote access only / transit only; encryption state and key custody}}
- Frequency and duration: {{one-off / continuous; contract term}}
- Transfer tool used: {{IDTA / UK Addendum to EU SCCs / BCRs}} — reference: {{…}}

## Step 2 — Assess the risk profile of the data

For these data and subjects, what could go wrong for individuals if the data were accessed unlawfully or the importer failed to honour the tool? {{Score harm realistically: identity fraud potential, discrimination, persecution risk for the specific subjects, physical safety, distress. Low-risk business-contact data ≠ health data of vulnerable people.}}

## Step 3 — Assess the destination regime (outcome-focused)

> You are asking whether, **in practice and for this transfer**, protection would be materially lower — considering respect for the rule of law, relevant surveillance and government-access laws and their real-world application to this importer/sector, the enforceability of the transfer tool's contractual rights, and available redress for UK data subjects.

- Importer's sector and any local law obligations to disclose data to authorities: {{…}}
- Realistic likelihood of government access to **this** data, based on the importer's sector, data type and history: {{…}}
- Can the importer honour the IDTA/Addendum obligations (challenge unlawful requests, notify the exporter where permitted)? {{importer's statements, transparency reports}}
- Enforceability and redress: {{can data subjects enforce the tool's third-party rights; is there any avenue of complaint or compensation in the destination}}

## Step 4 — Supplementary measures (if Step 3 raises concerns)

{{Technical: end-to-end or in-transit+at-rest encryption with keys held only in the UK; pseudonymisation before transfer; split processing. Contractual: enhanced audit, notification and challenge duties. Organisational: data minimisation before export, access controls, transfer logging.}}

## Step 5 — Decision

| | |
|---|---|
| Conclusion | {{Protection is not materially lower — proceed with the tool / proceed with the supplementary measures in Step 4 / do NOT transfer}} |
| Reasoning (3–5 sentences, outcome-focused) | {{…}} |
| Conditions and monitoring | {{what would trigger re-assessment — legal change in destination, importer breach, new sub-processor}} |
| Sign-off | {{name, role, date}} |

> Record this TRA with the executed IDTA/Addendum and reference both from the RoPA row for this processing (Art 30(1)(e)) and, at category level, in the privacy notice (Art 13(1)(f)).
