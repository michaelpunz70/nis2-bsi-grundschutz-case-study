# Source Verification Notes

Cases where a regulatory or technical claim — including AI-generated suggestions — was checked against the primary source (legal text or BSI Kompendium) before being accepted. Documents where verification caught or prevented an error.

---

### SV-01 · §28 Abs. 2 BSIG — size thresholds for "wichtige Einrichtung"
- **Milestone:** M1
- **Claim under check:** an AI suggestion phrased the Executive Summary as "any single criterion suffices" (≥50 employees OR >€10M turnover OR >€10M balance sheet).
- **Primary source checked:** § 28 Abs. 2 BSIG (official legal text).
- **Finding:** the law uses "und" + "jeweils" — ≥50 employees, OR annual turnover AND balance sheet total each above €10M. The two financial thresholds are cumulative, not alternative.
- **Impact:** a firm with 20 employees, €15M turnover and €4M balance sheet would be wrongly pulled into scope under the AI phrasing. Rejected and corrected before commit (v1.1).
- **My note (my words):** "From personal experience, you cannot trust an AI's paraphrase when it comes to legal logic—conjunctions like 'und' or 'oder' and terms like 'jeweils' must be read directly in the literal text. Skipping this check can lead to serious mistakes, such as a wrong NIS2 applicability classification, which carries not only legal consequences but also real risks for company security. Always keep the legislative texts within reach."
- **Status:** Corrected — 01_NIS2_Betroffenheitsanalyse v1.1

---

### SV-02 · §28 Abs. 1 BSIG — upper threshold ("besonders wichtige Einrichtung")
- **Milestone:** M1
- **Claim under check:** an AI correction applied the generic EU "large enterprise" logic, treating the financial thresholds as alternative.
- **Primary source checked:** § 28 Abs. 1 BSIG.
- **Finding:** "und" — the upper threshold is ≥250 employees, OR turnover >€50M AND balance sheet total >€43M (both financial values cumulative). The generic-EU reading did not match the German text.
- **Impact:** prevented a wrong threshold logic from entering the classification reasoning (v1.1).
- **My note (my words):** "Here the model didn't just make a vague claim—it confidently 'corrected' me with a generic EU rule that sounded completely plausible, yet was wrong under German law. A confident tone is not a primary source: even when an AI pushes back with authority, its numbers and logic must be verified against the original text."
- **Status:** Corrected — 01_NIS2_Betroffenheitsanalyse v1.1

---

### SV-03 · BSI Kompendium — correct OPS module numbering (current edition)
- **Milestone:** M2 (forward-reference to M3)
- **Claim under check:** an AI reference cited "OPS.2.1 Outsourcing für Kunden" for the outsourcing module.
- **Primary source checked:** current IT-Grundschutz-Kompendium, group OPS.2 "Betrieb von Dritten" (via NotebookLM).
- **Finding:** in the current edition the relevant customer-side modules are OPS.2.2 Cloud-Nutzung and OPS.2.3 Nutzung von Outsourcing; the "OPS.2.1" reference reflected an outdated edition.
- **Impact:** DEC-05's module references were aligned to the current Kompendium instead of an obsolete numbering.
- **My note (my words):** "When checking the module number suggested by the AI, it turned out to be wrong—not because the model was hallucinating, but because it pulled a real module number from an outdated edition of the Kompendium before it was renumbered. Official standards undergo updates that AI models aren't always aligned with, so checking against the current edition is essential."
- **Status:** Verified — referenced in decision-log DEC-05

---

### SV-04 · Applicable entry-into-force date — national law vs EU directive deadline
- **Milestone:** M1
- **Claim under check:** which date governs applicability and obligations — the EU NIS2 Directive's transposition deadline (17 Oct 2024) or the German implementing law's entry into force?
- **Primary source checked:** NIS2-Umsetzungs- und Cybersicherheitsstärkungsgesetz (NIS2UmsuCG) — the national implementing law. 
- **Finding:** a directive is not directly applicable — it requires national transposition. Germany missed the EU transposition deadline (17 Oct 2024); the national law (NIS2UmsuCG) entered into force on 6 Dec 2025. Müller's obligations therefore key to the national Inkrafttreten (6 Dec 2025), not the EU deadline.
- **Impact:** confirmed the reference date underpinning the "ab sofort" registration timing (see DEC-02); avoided anchoring obligations to the (missed) EU deadline or assuming direct applicability of the directive.
- **My note (my words):** "Whenever EU directives are involved, you must always check when the national transposition actually enters into force in the country where the company is based—not just in Germany, but across any EU member state, since each country sets its own effective date. Here, the governing text is the German NIS2UmsuCG, not the EU deadline; getting this wrong would have meant prematurely triggering obligations or citing the wrong legal basis to the Geschäftsführung."
- **Status:** Confirmed — 01_NIS2_Betroffenheitsanalyse v1.1
