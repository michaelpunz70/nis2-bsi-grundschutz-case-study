# Decision Log

Key methodological and classification decisions, with the reasoning behind each. Illustrative of how choices were made under incomplete information.

---

### DEC-01 · Classification as "wichtige Einrichtung" (Important Entity)
- **Milestone:** M1 — Legal Scope & Registration
- **Question:** Is Müller Maschinenbau GmbH classified as a "besonders wichtige Einrichtung" (Essential Entity) or a "wichtige Einrichtung" (Important Entity) under the German implementation of NIS2 (BSIG)?
- **Options:** (a) Treat as a "besonders wichtige Einrichtung" (Essential Entity) based on overall sector criticality; (b) Classify strictly as a "wichtige Einrichtung" (Important Entity) based on NACE sector classification (C28 — Machinery and equipment) and medium enterprise size thresholds.
- **Decision:** (b) — Wichtige Einrichtung.
- **Rationale (my words):** "While manufacturing feels critical from a supply chain perspective, the law draws a hard line based on NACE codes (Anlage 2 BSIG). Since we fall under mechanical engineering (C28), we are designated as a wichtige Einrichtung, meaning we cannot be elevated to 'besonders wichtig' status regardless of company size. This shapes our compliance burden—focusing on ex-post enforcement rather than ex-ante supervision."
- **Status:** Approved — 01_NIS2_Betroffenheitsanalyse v1.2

---

### DEC-02 · BSI Registration Timeline ("Ab sofort")
- **Milestone:** M1 — Legal Scope & Registration
- **Question:** When must the registration with the BSI portal be initiated under the updated timeline?
- **Options:** (a) Within 3 months of hitting thresholds (old interpretation); (b) "Ab sofort" (immediately upon applicability, considering the BSIG entry into force on December 6, 2025).
- **Decision:** (b).
- **Rationale (my words):** "With the legal framework fully live as of December 2025, waiting for a grace period is a compliance liability. Registration is a mandatory baseline prerequisite before diving into deep technical risk assessments; it establishes our accountability posture right from Milestone 1."
- **Status:** Approved — 01_NIS2_Betroffenheitsanalyse v1.2

---

### DEC-03 · Scope Built from Business Processes, Not from Systems
- **Milestone:** M2 — Strukturanalyse (Informationsverbund / information domain)
- **Question:** Build the Informationsverbund starting from IT systems (servers, clients, OT) or from the Geschäftsprozesse (business processes)?
- **Options:** (a) List systems first and draw the perimeter around them; (b) Start from core business processes (GP-01 to GP-11) and cascade downwards to applications → systems → networks → rooms (BSI 200-2, Ch. 7.1).
- **Decision:** (b).
- **Rationale (my words):** "I first reasoned from the servers and physical hardware, but true risk criticality originates in the business process and propagates downward. Scoping bottom-up from systems would have hidden which assets actually matter to the company's survival. Starting top-down from Geschäftsprozesse ensures our security perimeter aligns strictly with business value."
- **Status:** Approved — 02_Strukturanalyse_Schutzbedarf v1.1

---

### DEC-04 · Inclusion of Operational Technology (OT) in the Perimeter
- **Milestone:** M2 — Strukturanalyse (Informationsverbund)
- **Question:** Should the OT environment (CNC machines, MES terminal) be included in the scope despite being physically on the shop floor?
- **Options:** (a) Exclude OT, treating it as traditional mechanical engineering outside cybersecurity scope; (b) Fully include OT because the production network is physically linked to the IT infrastructure, qualifying it as part of the legal "Netz- und Informationssysteme" under § 30 BSIG that support critical business processes within the BSI 200-2 Informationsverbund.
- **Decision:** (b).
- **Rationale (my words):** "Even though the production manager argued 'everything is fine' and internet isn't needed in the hall, the reality is that the flat network bridges IT and office systems directly to the shop floor via USB sticks and shared switches. Legally and methodologically, you cannot secure the enterprise while ignoring the factory floor when it directly supports core manufacturing processes."
- **Status:** Approved — 02_Strukturanalyse_Schutzbedarf v1.1

---

### DEC-05 · CloudSecure Backup Included as External Interface (Shared Responsibility)
- **Milestone:** M2 — Strukturanalyse (Informationsverbund & Interfaces)
- **Question:** How should the external backup provider (CloudSecure GmbH) be modeled within the asset structure?
- **Options:** (a) Treat them as an external black box outside our operational perimeter; (b) Model them explicitly as an external interface with a shared responsibility profile, recognizing its criticality for business continuity.
- **Decision:** (b).
- **Rationale (my words):** "Outsourcing backup to a third party via an encrypted VPN tunnel doesn't outsource our ultimate legal accountability under NIS2. CloudSecure is a critical dependency—if their infrastructure fails or is compromised, our recovery capability vanishes. It must be explicitly mapped as a high-risk interface, paving the way for operational third-party and cloud controls in Milestone 3 (specifically targeting BSI OPS.2.2 Cloud-Nutzung and OPS.2.3 Nutzung von Outsourcing)."
- **Status:** Approved — 02_Strukturanalyse_Schutzbedarf v1.1

---

### DEC-06 · proAlpha ERP Anticipated as High/Very High Protection Need (Maximumprinzip)
- **Milestone:** M2 — Strukturanalyse (Schutzbedarf / protection requirements anticipation)
- **Question:** How should the criticality of core enterprise systems like proAlpha ERP be provisionally weighted before formal evaluation?
- **Options:** (a) Treat it as a standard software application with normal availability requirements; (b) Anticipate a "Hoch / Sehr hoch" protection need due to its transversal usage across almost all core business processes, applying the Maximumprinzip (maximum principle) criterion by criterion.
- **Decision:** (b).
- **Rationale (my words):** "Because proAlpha touches everything from order entry and purchasing to logistics and financial accounting, applying the BSI Maximumprinzip means its availability and integrity cannot be compromised. Any prolonged outage here paralyzes the entire company, meaning its baseline protection requirements must be set high right from the start. (Note: Kept provisional for Milestone 2; formal Schutzbedarfsfeststellung follows in the next step)."
- **Status:** Approved — 02_Strukturanalyse_Schutzbedarf v1.1

---

### DEC-07 · Personalleitung Office Carved Out as Separate Room R-08 (Art. 9 GDPR Data)
- **Milestone:** M2 — Strukturanalyse (Räume / physical scope)
- **Question:** How should the physical BEM files (special-category health data under Art. 9 GDPR) held at the Personalleitung be modeled — within the general office building (R-01) or as a dedicated room?
- **Options:** (a) Keep them within R-01 and accept that the whole office building inherits "sehr hoch" confidentiality; (b) Carve out a dedicated room R-08 for the Personalleitung office, move HR/GP-09 there, and adjust R-01 accordingly.
- **Decision:** (b).
- **Rationale (my words):** "I chose option (b) because if we left the physical BEM files inside the general office building R-01, the Maximumprinzip would force the entire building's confidentiality up to 'sehr hoch' just because of one HR cabinet. By carving out the Personalleitung office as a dedicated room (R-08), we isolate the 'sehr hoch' requirement strictly where the Art. 9 data lives and keep R-01 properly proportioned. Saying 'it's locked in a cabinet' doesn't bypass the Grundschutz rules here—we need the physical separation. I'll verify the physical access controls and locking mechanisms during M3."
- **Status:** Approved — 02_Strukturanalyse_Schutzbedarf v1.1
