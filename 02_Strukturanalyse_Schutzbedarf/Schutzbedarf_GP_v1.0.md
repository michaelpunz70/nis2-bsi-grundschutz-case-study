# Schutzbedarfsfeststellung — Geschäftsprozesse

**Referenz:** BSI-Standard 200-2, Kap. 8.2.3 · **Grundlage:** Schadensszenarien-Skala v1.1

---

| ID | Geschäftsprozess | C | I | A | Begründung (mit Schadensszenario) | Gesamt (Driver) |
|:---|:-----------------|:-:|:-:|:-:|:----------------------------------|:---------------:|
| **GP&#8209;01** | Unternehmensführung | Hoch | Hoch | Normal | C/I: Strategische Unternehmensdaten, Finanzpläne und M&A-Unterlagen (Szenario 1/5). A: Kurzzeitiger Ausfall stört nur operativ, rechtfertigt kein Hoch (Szenario 4). | Hoch (C/I) |
| **GP&#8209;02** | Compliance & NIS2 | Hoch | Hoch | Normal | I: Manipulation von Audit-Dokumenten oder NIS2-Meldungen führt zu schweren Bußgeldern und Sanktionen, gefährdet aber nicht das Existenzende (Szenario 1). | Hoch (I) |
| **GP&#8209;03** | Konstruktion & Entwicklung | Sehr hoch | Hoch | Hoch | C: Umfasst sensible CAD-Konstruktionen und Patentanmeldungen; Abfluss an Konkurrenz ist existenzbedrohend (Szenario 5). | Sehr hoch (C) |
| **GP&#8209;04** | Arbeitsvorbereitung (AV) | Sehr hoch | Sehr hoch | Hoch | C: Verarbeitet die sehr hohen CAD-Daten und Fertigungs-Know-how (Szenario 5). I: CNC-Programmierfehler bergen Safety-Risiken (Szenario 3). | Sehr hoch (C/I) |
| **GP&#8209;05** | CNC-Fertigung | Normal | Sehr hoch | Sehr hoch | I: Physische Maschinensteuerung / Safety (Szenario 3). A: Stillstand > 2 Tage löst den Vertragsbruch mit dem Hauptkunden aus (> 250k €, Szenario 4 & 6). | Sehr hoch (I/A) |
| **GP&#8209;06** | Vertrieb | Hoch | Hoch | Hoch | C/I: Kundendaten und Verträge. A: Ausfall verzögert den Vertrieb, bleibt aber im Rahmen der operativen Toleranz (Szenario 4 & 6). | Hoch (C/I/A) |
| **GP&#8209;07** | Versand & Logistik | Normal | Hoch | Hoch | A: Ein IT-Ausfall im Versand ist durch manuelle Lieferscheine und Lagerpuffer für 24–48 Std. überbrückbar; kein sofortiger existenzbedrohender Vertragsbruch (Szenario 4 & 6). | Hoch (A) |
| **GP&#8209;08** | IT- & OT-Betrieb | Sehr hoch | Sehr hoch | Sehr hoch | C: Kumulationseffekt / erweiterter Administrationsschutz (Zugriff auf AD, Backups, CAD und BEM-Akten). I/A: Zentraler Betrieb von ERP/MES. | Sehr hoch (C/I/A) |
| **GP&#8209;09** | Personalwesen (HR) | Sehr hoch | Hoch | Normal | C: Zwingend sehr hoch aufgrund digitaler/physischer BEM-Akten mit Gesundheitsdaten nach Art. 9 DSGVO (Szenario 2 / A-13). | Sehr hoch (C) |
| **GP&#8209;10** | Finanz- & Rechnungswesen | Hoch | Hoch | Hoch | I: Manipulationen im Zahlungsverkehr führen zu spürbaren finanziellen Schäden, sind aber für das Unternehmen verkraftbar (Szenario 1 & 6). | Hoch (I) |
| **GP&#8209;11** | Einkauf & Lagerhaltung | Normal | Hoch | Hoch | I: Manipulierte Lieferanten-/Bestandsdaten verfälschen Beschaffung. A: Lagerpuffer fangen kurzfristige Ausfälle ab; längerer Stillstand bremst die Produktion (Szenario 4). | Hoch (I/A) |

---

**Version:** v1.0 — Erste Schutzbedarfsfeststellung der Geschäftsprozesse (GP-01–GP-11); Grundlage: Schadensszenarien-Skala v1.1.
