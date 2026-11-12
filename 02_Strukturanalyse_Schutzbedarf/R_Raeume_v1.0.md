# Räume und Standorte — Müller Maschinenbau GmbH

**Geltungsbereich:** Informationsverbund Müller Maschinenbau GmbH

---

| ID | Raum / Bereich | Zugeordnete SYS & Personen | Beschreibung / Funktion | Physische Sicherheit & Besonderheiten |
|:---|:---------------|:---------------------------|:------------------------|:--------------------------------------|
| **R&#8209;01** | Bürogebäude & Verwaltung | SYS&#8209;04 (ca. 40 Büro-PCs), Geschäftsführung, Vertrieb, HR, Buchhaltung | Klassische Büroarbeitsplätze für die kaufmännischen und administrativen Prozesse (GP&#8209;01, GP&#8209;02, GP&#8209;09, GP&#8209;10) | Normaler Bürozutritt (Schlüssel / Schloss); Publikumsverkehr im Empfangsbereich |
| **R&#8209;02** | Konstruktionsbüro (CAD / AV) | SYS&#8209;04b (ca. 5 CAD-Workstations), Konstrukteure, Arbeitsvorbereitung | Spezieller Bürobereich für CAD/CAM-Planung und Arbeitsvorbereitung (GP&#8209;03, GP&#8209;04) | Höherer Schutzbedarf der Daten (Schutz geistigen Eigentums / Konstruktionspläne) |
| **R&#8209;03** | Serverraum / Technikraum | SYS&#8209;01 (DC), SYS&#8209;02 (Fileserver), SYS&#8209;03 (proAlpha ERP), SYS&#8209;06 (Firewall), Switches | Zentraler, geschlossener Raum für die gesamte IT-Infrastruktur und Kernkomponenten | Kritisch: Physische Absicherung (Zutrittsbeschränkung, Klimatisierung, Brandschutz, USV) |
| **R&#8209;04** | Produktionshalle (Fertigung) | SYS&#8209;08 (MES-Rechner), SYS&#8209;09 (8 CNC-Maschinen & Terminals), Produktionsmitarbeiter | Große Industriehalle für die spanende Bearbeitung (Fräsen, Drehen) und Auftragssteuerung vor Ort (GP&#8209;04, GP&#8209;05) | Industriehallen-Zutritt (Mitarbeiter / befugte Dienstleister); Maschinen direkt zugänglich |
| **R&#8209;05** | Lager & Versand | SYS&#8209;04 (Teilmenge / ERP-Clients), Lager- und Versandpersonal | Bereich für Wareneingang, Materiallagerung, Kommissionierung und Warenausgang / Lieferscheinerstellung (GP&#8209;06, GP&#8209;07) | Offener Logistikbereich mit regelmäßigem Lieferverkehr und externen Spediteuren |
| **R&#8209;06** | Konferenz- / Besprechungsräume | SYS&#8209;07 (WLAN-APs), interne Mitarbeiter, externe Besucher (Kunden, Lieferanten, Partner) | Räumlichkeiten für Meetings, Präsentationen und Verhandlungen | Risiko: Externer Zutritt, Gefahr von Shoulder Surfing und ungesichertem physischen Netzwerkzugang |
| **R&#8209;07** | Mobiler Arbeitsplatz / Häusliches Arbeitsumfeld | SYS&#8209;05 (8 Außendienst-Notebooks), Außendienstmitarbeiter | Dezentrale Arbeitsorte außerhalb des Firmenperimeters (Home Office, Hotels, Kundenstandorte vor Ort) | Unkontrollierte physische Umgebung: Kein direkter Einfluss des Unternehmens auf die physische Sicherheit vor Ort (BSI INF.8 / INF.9) |

---

## Offene Fragen an Stakeholder

### 1. An den IT-Leiter (Jens Hoffmann)

- **Zutrittskontrolle Serverraum (R-03):** Wie ist der Serverraum physisch gesichert (z. B. elektronisches Zutrittskontrollsystem mit Protokollierung, klassischer Bartschlüssel, Brandschutzeinrichtungen, USV)?
- **Gäste-WLAN / Konferenzräume (R-06):** Gibt es in den Konferenzräumen dedizierte Netzwerkdosen für Gäste oder ein isoliertes Gäste-WLAN, das physisch/logisch vom internen Firmennetz getrennt ist?

### 2. An den IT-Leiter / Geschäftsführung

- **Home Office & Mobile Geräte (R-07):** Gibt es für die 8 Außendienst-Mitarbeiter / Home-Office-Arbeitsplätze verbindliche Sicherheitsrichtlinien (z. B. Verbot der Nutzung durch Familienangehörige, automatische Bildschirmsperre, VPN-Pflicht)?
