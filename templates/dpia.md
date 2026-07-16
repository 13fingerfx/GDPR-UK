# Data Protection Impact Assessment (DPIA) — Template (UK GDPR Art 35)

> Mirrors the ICO's Sample DPIA template (`sources/ico-dpia-template.docx`, Steps 1–7); a completed worked example is at `sources/ico-dpia-example-completed.pdf`. Do the DPIA **before** processing starts, integrate outcomes into the project plan, and review it when risk changes (Art 35(11)).
>
> **When required** (Art 35(1), (3) + ICO high-risk list, `sources/ico-dpia-high-risk-list.pdf`): systematic and extensive profiling with significant effects; large-scale special category or criminal offence data; large-scale systematic monitoring of public areas; and ICO-listed operations including innovative technology/AI, biometrics for identification, geolocation tracking, invisible processing, data matching, targeting children or vulnerable people, and denial of service based on profiling.

| Document control | |
|---|---|
| Project / processing name | {{…}} |
| Author / owner | {{name, role}} |
| DPO advice sought (Art 35(2)) | {{date, name}} |
| Version / date / review date | {{…}} |

## Step 1: Identify the need for a DPIA

{{Explain broadly what the project aims to achieve and what type of processing it involves. State which Art 35(3)/ICO-list trigger applies, or why you are doing a DPIA voluntarily. Link screening questions if used.}}

## Step 2: Describe the processing

- **Nature**: {{how data is collected, used, stored, deleted; source; sharing; processors; high-level data flow — attach a diagram if available}}
- **Scope**: {{categories of personal data (flag special category/criminal offence data), volume, number of data subjects, geographical area, retention}}
- **Context**: {{relationship with data subjects; how much control they have; children or vulnerable groups; prior concerns or security flaws; novelty of the technology; current public concerns}}
- **Purposes**: {{what you achieve; benefits for you, individuals, society; if legitimate interests is the basis — state the interest}}

## Step 3: Consultation

{{How you have or will seek data subjects' views — or your reasoned justification for not doing so (Art 35(9)). Internal stakeholders consulted (security, engineering, legal). Processors consulted. Whether independent experts are needed.}}

## Step 4: Assess necessity and proportionality

- Lawful basis: {{Art 6 basis; Art 9(2) + DPA 2018 Sch 1 condition if special category; Arts 22A–22D analysis if solely automated significant decisions — including how the Art 22C safeguards (information, representations, human intervention, contestability) will be delivered}}
- Could the purpose be achieved with less data or a less intrusive method? {{…}}
- Data quality and minimisation measures: {{…}}
- Information to data subjects (Arts 12–14): {{…}}
- How rights (Arts 15–21) will be supported in this processing: {{…}}
- Processor compliance (Art 28) and international transfers (Ch V — mechanism per destination): {{…}}

## Step 5: Identify and assess risks

> Score each risk to **individuals** (not to the organisation): likelihood (remote / possible / probable) × severity (minimal / significant / severe) → overall (low / medium / high).

| # | Source of risk and nature of potential impact on individuals | Likelihood | Severity | Overall |
|---|---|---|---|---|
| 1 | {{e.g. unauthorised access to health data via over-broad staff permissions → distress, discrimination}} | {{…}} | {{…}} | {{…}} |
| 2 | {{e.g. re-identification of pseudonymised records when combined with X}} | {{…}} | {{…}} | {{…}} |
| 3 | {{e.g. automated decision wrongly denies service; no effective route to contest}} | {{…}} | {{…}} | {{…}} |

## Step 6: Identify measures to reduce risk

| Risk # | Measure | Effect on risk | Residual risk | Approved |
|---|---|---|---|---|
| 1 | {{e.g. role-based access + access reviews quarterly}} | {{reduced}} | {{low}} | {{Y/N}} |
| 2 | {{…}} | {{…}} | {{…}} | {{…}} |

## Step 7: Sign-off and outcomes

| Item | Name / date / notes |
|---|---|
| Measures approved by | {{…}} |
| Residual risks approved by | {{…}} — **if any residual risk remains HIGH, you must consult the ICO before processing (Art 36); you cannot sign it off internally** |
| DPO advice provided | {{summary}} |
| DPO advice accepted or overruled | {{if overruled — reasons}} |
| Consultation responses reviewed | {{…}} |
| This DPIA will be kept under review by | {{owner; review trigger/date}} |
