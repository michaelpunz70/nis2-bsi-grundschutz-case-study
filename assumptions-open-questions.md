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
- **Milestone:** M2 · **Type:** Closed (was Open)
- **What we knew:** DATEV was not explicitly named by stakeholders (typical for a German Mittelstand). It was unclear whether accounting data is exported from proAlpha to the external tax advisor's DATEV or maintained internally, and whether payroll (GP-09) is handled in-house or outsourced to the Steuerberater.
- **Why it matters:** determines whether DATEV is an in-scope application (APP) or an external dependency. Export-only means no DATEV instance in Müller's Informationsverbund.
- **Working assumption (while open):** export-only — later confirmed.
- **Resolution:** IT-Leiter Hoffmann confirmed — the Buchhaltung exports the accounting entries from proAlpha once a month and emails the file to the external Steuerberater; DATEV runs only at the tax advisor, not internally. Payroll follows the same external route.
- **Owner / action:** IT-Leiter — confirmed.
- **Status:** Closed — confirmed by IT-Leiter (stakeholder email, M2)

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

---

### A-09 · Production downtime — financial impact per day
- **Milestone:** M2 · **Type:** Closed
- **What we know:** Geschäftsführung confirmed — a full day of standstill costs ca. €80,000–100,000 (lost orders + contractual penalties); from day 3, breach of contract with the main OEM customer (~35% of turnover).
- **Why it matters:** key input for the Schutzbedarfsfeststellung — Verfügbarkeit (availability) of the production processes (GP-03/GP-04) and the financial damage scenario.
- **Resolution:** daily production loss ≈ €80–100k; contractual-breach risk from day 3.
- **Owner / action:** Geschäftsführung — confirmed.
- **Status:** Closed — confirmed by GF (stakeholder email, M2)

---

### A-10 · ERP backup — RPO confirmed, restore untested 🔴
- **Milestone:** M2 · **Type:** Closed (with residual risk)
- **What we know:** IT-Leiter — the CloudSecure backup runs nightly, so the RPO is at most 24h; but a full restore has never been tested.
- **Why it matters:** the 24h RPO is confirmed, but an untested restore means the actual recovery time is unknown — a red flag for the Verfügbarkeit assessment and a Gap to carry into M3.
- **Resolution:** RPO = 24h (confirmed); recoverability and actual recovery time = unknown (restore never tested) — treated as an assumption, not evidence.
- **Owner / action:** IT-Leiter (RPO confirmed); add a restore test as a measure in M5.
- **My note (my words):** "The information I have received is that the RPO is 24h. What is not established is whether those backups can actually be restored at all, and how long recovery would take. Without a demonstrable restore test, recoverability is a hope, not a proven control: only the test would produce evidence of the actual recovery time (RTA) to compare against the target (RTO) — right now that figure is assumed, not measured. I treat it as a gap / residual risk to carry into M3 and a measure (restore test) in M5, not as evidence."
- **Status:** Closed — RPO confirmed; untested restore flagged for M3/M5

---

### A-11 · MES failure — impact on production
- **Milestone:** M2 · **Type:** Closed
- **What we know:** Produktionsleiter Berger — if the MES fails, production can continue on paper for ca. 2–3 hours; after that the machines stop.
- **Why it matters:** defines the Verfügbarkeit threshold for GP-03/GP-04 and SYS-08 (MES).
- **Resolution:** MES failure → 2–3h paper fallback, then full production stop.
- **Owner / action:** Produktionsleiter — confirmed.
- **Status:** Closed — confirmed by Produktionsleiter (stakeholder email, M2)

---

### A-12 · CNC program manipulation — safety risk 🔴
- **Milestone:** M2 · **Type:** Closed (red flag)
- **What we know:** Produktionsleiter Berger — manipulated CNC programs are only noticed once scrap parts appear; at the tolerances involved (±0.01mm) a wrong program can also cause tool breakage, dangerous for the operators.
- **Why it matters:** elevates the Integrität (integrity) of the CNC/OT processes to "sehr hoch" (Schadensszenario 3: persönliche Unversehrtheit / personal safety) — the strongest driver for "sehr hoch" in the whole Informationsverbund.
- **Resolution:** Integrität of CNC/OT = sehr hoch, driven by operator-safety impact.
- **Owner / action:** Produktionsleiter — confirmed; feeds directly into the Schutzbedarfsfeststellung.
- **My note (my words):** "The reason to classify this as 'sehr hoch' is that an integrity breach here is not a data or business problem, but operator safety: a manipulated CNC program can cause tool breakage and physical harm. Detection is only after the fact, once scrap parts appear, so there is no preventive control today. This overrides the Produktionsleiter's 'everything is fine' stance — safety is not negotiable. The missing detection/prevention control is carried as a gap into M3, with treatment options assessed in M4/M5."
- **Status:** Closed — confirmed by Produktionsleiter (stakeholder email, M2)
