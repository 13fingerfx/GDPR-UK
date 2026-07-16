# Personal Data Breach Notification to the ICO — Template (UK GDPR Art 33)

> **Deadline: without undue delay and, where feasible, within 72 hours of becoming aware** (weekends included). If you don't have everything, notify in phases (Art 33(4)) — do not wait for a complete picture. If notifying late, include reasons (Art 33(1)). Use the ICO's online reporting service or 0303 123 1113; this template assembles the required content. Assess risk with `sources/ico-breach-assessing-guide.pdf`.
>
> If the breach is **unlikely to result in a risk** to individuals, you need not notify — but you must still record it internally (Art 33(5)): use the internal log section at the end. If in doubt, notify.

## Notification content [Art 33(3)]

**1. Organisation and contact**
- Controller: {{name, address, ICO registration number}}
- Contact for this breach: {{DPO or contact point — name, email, phone}} [33(3)(b)]
- Reporting on behalf of a controller as processor? {{No — processors notify their controller, not the ICO (Art 33(2)) / details of instruction}}

**2. When and how**
- Date/time breach occurred: {{…}}
- Date/time we became **aware** (and how): {{…}} — the 72h clock runs from here
- If this notification is later than 72h after awareness: reasons for delay: {{…}} [33(1)]
- Is this a phased/initial or complete notification? {{initial — further information to follow by {{date}} / complete}} [33(4)]

**3. Nature of the breach** [33(3)(a)]
- What happened: {{concise factual narrative — e.g. misdirected email; ransomware with exfiltration; lost unencrypted laptop; unauthorised access via credential stuffing}}
- Breach type: {{confidentiality / integrity / availability — one or more}}
- Categories of data subjects and **approximate number**: {{e.g. ~2,400 customers; 15 employees}}
- Categories of personal data and **approximate number of records**: {{…; flag special category or criminal offence data, financial data, credentials, children's data}}
- Was the data protected (encryption, hashing, remote wipe)? {{state honestly, with key-compromise status}}

**4. Likely consequences** [33(3)(c)]
{{Realistic assessment of what could happen to individuals: fraud/identity theft, financial loss, distress, discrimination, physical safety, loss of confidentiality. State likelihood and severity, not just possibilities.}}

**5. Measures taken or proposed** [33(3)(d)]
- Containment already taken: {{e.g. access revoked, systems isolated, recall attempted, passwords reset}}
- Mitigation for individuals: {{e.g. forced password reset, credit monitoring offered, warning sent}}
- Remediation to prevent recurrence: {{…}}
- Have affected individuals been told? {{Yes on {{date}} / planned {{date}} / no — reasoning against Art 34 (see below) }}

**6. Cross-border and other regulators**
{{EU data subjects affected → consider EU GDPR Art 33 notification to relevant EU SA. Sector duties: FCA, NCSC, action fraud, etc.}}

## Art 34 decision — telling individuals

High risk to individuals? {{Yes → notify affected individuals without undue delay using `templates/breach-notification-individuals.md` / No → record reasoning}}
Exceptions relied on (if any): {{data unintelligible (e.g. encrypted, keys safe) — 34(3)(a) / subsequent measures removed the high risk — 34(3)(b) / disproportionate effort → public communication — 34(3)(c)}}

## Internal breach log entry [Art 33(5)] — complete for EVERY breach, reported or not

| Field | Entry |
|---|---|
| Reference / date logged | {{…}} |
| Facts of the breach | {{…}} |
| Effects | {{…}} |
| Remedial action taken | {{…}} |
| ICO notified? | {{Y — date/reference / N — reasoned justification that risk is unlikely}} |
| Individuals notified? | {{Y/N + reasoning}} |
