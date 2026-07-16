# Record of Processing Activities (RoPA) — Controller Template (UK GDPR Art 30(1))

> One row per **processing activity** (not per system). Keep it owned, dated and versioned — the RoPA is the ICO's first ask in an audit. Processors: use the official ICO workbook at `sources/ico-ropa-template-processor.xlsx` instead (Art 30(2) requires a shorter record).
>
> The Art 30(5) exemption (fewer than 250 employees) is lost for any processing that is non-occasional, risky, or involves special category/criminal offence data — in practice, assume you need this record.

## Organisation block (complete once)

| Field | Entry | Authority |
|---|---|---|
| Controller name and contact details | {{…}} | Art 30(1)(a) |
| Joint controllers (if any) and arrangement summary | {{… / N/A}} | Art 30(1)(a), Art 26 |
| UK representative (if Art 27 applies) | {{… / N/A}} | Art 30(1)(a) |
| Data Protection Officer (if appointed) | {{… / N/A}} | Art 30(1)(a) |
| Document owner / last reviewed / version | {{name}} / {{date}} / {{v}} | Art 5(2) |

## Processing activity record (one per activity)

| Field | Entry | Authority |
|---|---|---|
| Activity name | {{e.g. Payroll; Customer CRM; CCTV; Recruitment}} | — |
| Purpose(s) of processing | {{…}} | Art 30(1)(b) |
| Lawful basis (recommended) | {{Art 6(1)(x); if 9(2) — condition + DPA 2018 Sch 1 para; if 6(1)(ea) — Annex 1 purpose}} | Art 6, 9, 10 |
| Categories of data subjects | {{e.g. employees, customers, website visitors}} | Art 30(1)(c) |
| Categories of personal data | {{…; flag special category and criminal offence data explicitly}} | Art 30(1)(c) |
| Categories of recipients | {{processors, group companies, regulators — incl. recipients in third countries}} | Art 30(1)(d) |
| Transfers to third countries / international organisations | {{destination + mechanism: adequacy / IDTA / UK Addendum / Art 49 derogation; safeguard documentation reference}} | Art 30(1)(e) |
| Retention period (or criteria) | {{…}} | Art 30(1)(f) |
| Security measures (general description) | {{e.g. encryption at rest/in transit, RBAC, MFA, logging, backup, testing — cross-reference security policy}} | Art 30(1)(g), Art 32 |
| Source of the data (recommended) | {{data subject directly / third party — which}} | supports Art 14 |
| DPIA required / reference (recommended) | {{yes → link / no → screening result}} | Art 35 |
| Processor contract reference (recommended) | {{link to Art 28 agreement}} | Art 28 |

> Rows marked "(recommended)" go beyond the Art 30 minimum but are standard ICO-aligned practice and make the record actually useful for DSARs, DPIAs and breach response.

## Common activities most organisations forget

HR and recruitment (including unsuccessful candidates), CCTV, website analytics and cookies, marketing lists, support tickets, supplier contacts, whistleblowing records, building access logs, backups as a distinct location, machine-learning training data.
