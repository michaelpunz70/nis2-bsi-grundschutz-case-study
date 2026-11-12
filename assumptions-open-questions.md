# Assumptions & Open Questions

Points left open or assumed during the assessment, with the working assumption used and who needs to confirm it. Shows how uncertainty was tracked rather than hidden.

---

### A-01 · Bilanzsumme (balance sheet total)
- **Milestone:** M1 · **Type:** Closed
- **What we knew:** not provided in the initial data; needed for the § 28 Abs. 2 size-threshold check.
- **Resolution:** ca. €18.5M, confirmed by the Geschäftsführung (CEO, T. Müller) — plausible against €22M turnover.
- **Impact:** completes the threshold check; classification unchanged (wichtige Einrichtung).
- **Status:** Closed — reflected in 01_NIS2_Betroffenheitsanalyse v1.2

---

### A-02 · Corporate structure (Konzernstruktur)
- **Milestone:** M1 · **Type:** Closed
- **What we knew:** unclear whether parent/subsidiary/partner entities would affect the size classification.
- **Resolution:** independent owner-managed GmbH; no group, no subsidiaries, no participations; sole shareholder T. Müller.
- **Impact:** no aggregation of headcount/financials → classification unchanged.
- **Status:** Closed — reflected in 01_NIS2_Betroffenheitsanalyse v1.2

---

### A-03 · proAlpha ↔ DATEV interface & payroll (Lohnabrechnung)
- **Milestone:** M2 · **Type:** Assumption / Open question
- **What we know:** DATEV (standard software used by tax advisors in Germany) was not explicitly named by stakeholders, though it is typical for a German Mittelstand. It is unclear whether accounting data is exported directly from proAlpha to the external tax advisor's DATEV system or maintained internally, and whether payroll (GP-09) is handled in-house or outsourced to the Steuerberater.
- **Why it matters:** determines the ownership of financial-data flows, whether payroll processing is in-scope internally or an external interface, and the Schutzbedarf (protection requirements) of the accounting process.
- **Working assumption:** direct export of accounting data from proAlpha to the tax advisor's DATEV account; payroll handling (internal vs. outsourced) to be confirmed.
- **Owner / action:** clarify with Buchhaltung (accounting) / Geschäftsführung.
- **Status:** Open

---

### A-04 · CAD/CAM software vendor
- **Milestone:** M2 · **Type:** Assumption
- **What we know:** no stakeholder named the CAD/CAM product.
- **Why it matters:** application-inventory (APP) entry; vendor influences later module/control selection.
- **Working assumption:** "CAD/CAM software (assumption: Autodesk Inventor or comparable)".
- **Owner / action:** confirm with Konstruktions- / IT-Leiter (head of design / head of IT).
- **Status:** Open (assumption flagged in the deliverable)

---

### A-05 · IT ↔ OT network segmentation 🔴
- **Milestone:** M2 · **Type:** Open question / red flag
- **What we know:** IT-Leiter Hoffmann — "Produktions-Netz hängt irgendwie auch am gleichen Netz, da müsste man mal schauen." Produktionsleiter (head of production) Berger refers the question back to Hoffmann.
- **Why it matters:** a flat IT/OT network removes a key security boundary; it drives the OT Schutzbedarf and the Risikoanalyse (risk analysis, BSI 200-3) — likely a single point of failure.
- **Working assumption:** treat IT and OT as connected (worst case).
- **Owner / action:** confirm segmentation with the IT-Leiter; candidate measure for the Realisierungsplan (implementation plan, M5).
- **My note:** "I must always anticipate a potential worst-case scenario during scoping, while waiting for concrete technical feedback from the IT-Leiter before finalizing the classification."
- **Status:** Open

---

### A-06 · CloudSecure shared global admin account 🔴
- **Milestone:** M2 · **Type:** Open question / red flag
- **What we know:** CloudSecure (Weber) — "für die M365-Administration nutzen wir denselben globalen Admin-Account wie Herr Hoffmann." Backup configuration details "müsste erst intern klären."
- **Why it matters:** a shared global admin account breaks least-privilege and accountability; affects identity & access controls and third-party risk.
- **Working assumption:** shared global admin in use until separated.
- **Owner / action:** obtain the backup configuration; require separate, personal accounts; feed into M3 (OPS modules) and M5.
- **My note:** "If this situation is confirmed to be true, it must be addressed as soon as possible by enforcing a strict least-privilege access control structure with separate, personal accounts."
- **Status:** Open

---

### A-07 · No ISMS tool in place
- **Milestone:** M2 · **Type:** Open item
- **What we know:** no dedicated ISMS tool exists to manage the Informationsverbund (information domain) / ISMS documentation.
- **Why it matters:** surfaces as a formal gap at M3 (Baustein ISMS.1 requires documented, traceable processes).
- **Working assumption:** documentation maintained manually for now.
- **Owner / action:** introduce an ISMS tool as a 0–3 month Sofortmaßnahme (immediate measure) in the Realisierungsplan (M5).
- **Status:** Open (carried to M5)

---

### A-08 · Arbeitsvorbereitung (CNC programming) placement
- **Milestone:** M2 · **Type:** To decide
- **What we know:** CNC programs reach the shop floor via USB from the Arbeitsvorbereitung (work preparation). Unclear whether this sub-process sits under GP-04 (Produktion) or GP-03 (Konstruktion).
- **Why it matters:** process mapping decides which Geschäftsprozess (business process) owns the USB data-transfer risk — a notable attack path.
- **Working assumption:** provisionally mapped under GP-04 (Produktion / Arbeitsvorbereitung). The USB transfer is treated as a security-relevant data path bridging the networked workstation and the shop floor, regardless of whether the CNC machines are air-gapped — their actual network isolation remains unconfirmed and is linked to A-05.
- **Owner / action:** assign in the business-process map.
- **Status:** Open / to decide
