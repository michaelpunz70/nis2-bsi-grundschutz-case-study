# Anwendungen — Müller Maschinenbau GmbH

**Geltungsbereich:** Informationsverbund Müller Maschinenbau GmbH

---

| ID | Anwendung | Typ / Betrieb | Unterstützte GP | Kurzbeschreibung |
|:---|:----------|:--------------|:----------------|:-----------------|
| **APP&#8209;01** | proAlpha ERP (inkl. HR-Modul) | On-Premise (Windows Server 2022) | GP&#8209;01, GP&#8209;06, GP&#8209;07, GP&#8209;09, GP&#8209;10, GP&#8209;11 | Zentrales ERP-System für Auftragsabwicklung, Lieferscheine/Versand, Einkauf, Lagerhaltung und Finanzbuchhaltung sowie Personalwirtschaft (HR-Modul mit BEM-Akten / Art.&#8201;9 DSGVO) |
| **APP&#8209;02** | Microsoft 365 (Exchange Online, SharePoint, Teams, OneDrive) | Cloud (SaaS) | GP&#8209;01 – GP&#8209;11 (alle) | Plattform für E-Mail-Kommunikation, Dokumentenablage und Kollaboration |
| **APP&#8209;03** | CAD/CAM-Software (Annahme: Autodesk Inventor o. ä.) | On-Premise (Workstations / Server) | GP&#8209;03, GP&#8209;04 | Software zur mechanischen/elektrischen Konstruktion sowie CAM-Programmierung (Annahme – Bestätigung erforderlich) |
| **APP&#8209;04** | MES (Manufacturing Execution System) | Lokal (eigener Rechner in der Produktion) | GP&#8209;04, GP&#8209;05 | System zur Auftragssteuerung, Fertigungsplanung und Produktionsüberwachung vor Ort |
| **APP&#8209;05** | DATEV (Annahme) | On-Premise / Cloud-Hybrid | GP&#8209;09, GP&#8209;10 | Fachsoftware für Finanzbuchhaltung sowie Lohn- und Gehaltsabrechnung (Annahme – ggf. Auslagerung an Steuerberater prüfen) |
| **APP&#8209;06** | Active Directory (AD) / DC | On-Premise (Windows Server 2019) | GP&#8209;01 – GP&#8209;11 (alle); verwaltet durch GP&#8209;08 | Zentraler Verzeichnis- und Authentifizierungsdienst für Benutzer-, Rechte- und Systemverwaltung |
| **APP&#8209;07** | Fileserver / Dateidienste | On-Premise (Windows Server 2019) | GP&#8209;01 – GP&#8209;11 (insb. Konstruktion & Verwaltung); verwaltet durch GP&#8209;08 | Zentrale Dateiablage (Netzlaufwerke) für Konstruktionsdaten, Geschäfts- und Verwaltungsdokumente |
| **APP&#8209;08** | CloudSecure Backup-Dienst | Cloud / Extern (CloudSecure GmbH) | GP&#8209;08 | Externer Backup-Dienst zur täglichen, verschlüsselten Datensicherung über VPN |
| **APP&#8209;09** | Unternehmens-Website (Annahme: externes Hosting) | Extern / Webhosting | GP&#8209;01, GP&#8209;06 | Öffentlicher Webauftritt zur Unternehmensdarstellung und Vertriebsunterstützung (Hosting und Zuständigkeit offen) |

---

## Offene Fragen

### An den IT-Leiter (Jens Hoffmann)
- **Fileserver (APP-07):** Welche Abteilungen bzw. Prozesse nutzen den Windows-Fileserver primär (z. B. Konstruktion, Verwaltung, Einkauf)?
- **MES & Active Directory (APP-04 / APP-06):** Ist das MES in der Produktion an das Active Directory angebunden oder läuft es komplett autark mit eigener Benutzerverwaltung?
- **Unternehmens-Website (APP-09):** Wer hostet und administriert unsere Unternehmens-Website?
- **Virenschutz / Security-Software:** Welche Antiviren- bzw. EDR-Lösung setzen wir auf den Servern und Clients ein?

### An den Produktionsleiter (Andreas Berger)
- **MES-Software (APP-04):** Wie heißt die eingesetzte MES-Software genau und von welchem Hersteller stammt sie?

### An den Konstruktionsleiter
- **CAD/CAM-Software (APP-03):** Welches konkrete CAD/CAM-System wird in der Konstruktion und Arbeitsvorbereitung eingesetzt?
- **Datenablage:** Wo werden die Konstruktions- und CAM-Daten gespeichert (Fileserver, eigener CAD-Server oder lokal)?

### An die Personalleitung (Frau Krause) & Leiter Finanzen
- **Abgrenzung proAlpha HR-Modul vs. DATEV (APP-01 / APP-05):** Welche Personaldaten werden im proAlpha HR-Modul geführt (inkl. BEM-Akten / Art. 9 DSGVO) und welche in DATEV? Wo liegt die Lohn- und Gehaltsabrechnung?
- **Zugriffsregelungen BEM-Akten:** Wer hat Zugriff auf die BEM-Akten im proAlpha HR-Modul sowie auf den physischen Aktenordner (vgl. A-13)?

### An den externen IT-Dienstleister (CloudSecure GmbH, Herr Weber)
- **Backup-Umfang (APP-08):** Welche Anwendungen und Datenbestände genau werden täglich gesichert (nur Server DC, Fileserver, proAlpha – oder auch M365 und MES)?

---

**Version:** v1.1 — APP-01 um GP-09 ergänzt (proAlpha HR-Modul mit BEM-Akten / Art. 9 DSGVO); offene Frage zu Zugriffsregelungen ergänzt. Quelle: GF-Mail vom 12.11.2026 (vgl. A-13).
