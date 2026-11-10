# NIS2-Betroffenheitsanalyse — Müller Maschinenbau GmbH

**Executive Summary** *(EN, 100–150 words)*

This assessment evaluates whether the company falls within the scope of the European NIS2 Directive and is therefore subject to mandatory registration with the German Federal Office for Information Security (BSI).

The applicability assessment considers three key criteria: the company's business sector, number of employees, and annual turnover or balance sheet total. As a general rule, companies operating in sectors covered by NIS2 may fall within its scope if they employ at least 50 people or exceed €10 million in annual turnover and annual balance sheet total.
However, certain entities may be subject to NIS2 obligations regardless of their size. Therefore, a comprehensive applicability assessment is required to determine the company's regulatory classification, registration obligations, and applicable cybersecurity risk management and incident reporting requirements under German law.

---

## 1. Grundlagen und Rechtsrahmen

Im Rahmen einer NIS-2-Betroffenheitsanalyse wird geprüft, ob das Unternehmen unter den Anwendungsbereich der NIS-2-Regulierung fällt und damit eine Registrierungspflicht beim Bundesamt für Sicherheit in der Informationstechnik (BSI) besteht.

Die Einstufung erfolgt anhand folgender Kriterien:

- Sektorzugehörigkeit
- Anzahl der Beschäftigten
- Jahresumsatz
- Jahresbilanzsumme

Werden die maßgeblichen gesetzlichen Kriterien und Schwellenwerte erfüllt, kann daraus eine verpflichtende Registrierung beim BSI resultieren. Die entsprechenden Registrierungspflichten gelten in Deutschland seit Inkrafttreten des nationalen NIS-2-Umsetzungsgesetzes am 6. Dezember 2025.

---

## 2. Klassifizierungsanalyse

### 2.1 Sektorale Einordnung
| Kriterium | Wert | Quelle / Begründung |
|---|---|---|
| Wirtschaftstätigkeit | Maschinenbau | E-Mail von Herr Müller |
| NACE-Code | C28 | https://nacecode.de/28-maschinenbau |
| NIS2-Anhang | Sonstige kritische Sektoren | Anlage 2 BSIG |
| Einrichtungstyp | Wichtige Einrichtung | NIS2 Art. 3 |

### 2.2 Größenschwellen (EU-KMU-Definition)
| Kriterium | Schwellenwert (NIS2) | Ist-Wert (Müller) | Überschritten? |
|---|---|---|---|
| Mitarbeiteranzahl | ≥50 | 148 | Ja |
| Jahresumsatz | >10 Mio. € | 22 Mio. € | Ja |
| Bilanzsumme | >10 Mio. € | offen (Rückfrage CEO) | k.A. |

---

## 3. Ergebnis der Betroffenheitsprüfung

| Frage | Ergebnis |
|---|---|
| Fällt das Unternehmen unter NIS2/BSIG? | Ja |
| Klassifikation | Wichtige Einrichtung |
| Registrierungspflicht beim BSI? | Ja |

---

## 4. Anwendbare Pflichten (BSIG)

| § BSIG | Pflicht | Frist | Bemerkung |
|---|---|---|---|
| §30 | Risikomanagement | Ab sofort | Abbildung des Unternehmens-IT-Systems mit Fokus auf Supply Chain - Prüfung des externen Cloud-Anbieters für Backups erforderlich |
| §32 | Meldepflicht | 24 Std (Early Warning) / 72 Std (Meldung) / 1 Monat (Bericht) an BSI | Interner Notfallprozess muss aufgebaut werden |
| §33 | Registrierungspflicht | Ab sofort | Formelle Registrierung mit Firmenname und Kontaktangaben für BSI  |
| §38 | Managementhaftung | Dauereinrichtung / Laufend | CEO muss formal informiert werden und Sicherheitsmaßnahmen genehmigen, um von eine persönliche Haft ausgeschlossen zu werden  |

---

## 5. Sofortmaßnahmen und Empfehlung an die Geschäftsführung

### 5.1 Kurzfristig (0–3 Monate) - Gesetzliche und Governance Dringlichkeiten
- [ ] Offizielle Registrierung beim BSI-Portal durchführen und Ansprechpartner benennen (§ 33 BSIG)
- [ ] Formale Information der Geschäftsführung über Haftungsrisiken sowie Freigabe des ISMS-Mandats (§ 38 BSIG)
- [ ] Provisorischen Meldeprozess für Sicherheitsvorfälle (24h/72h-Frist) etablieren (§ 32 BSIG)
- [ ] Erste Prüfung des externen Cloud-Backup-Anbieters (Verträge, SLAs, Sicherheitsstandards) (§ 30 BSIG)

### 5.2 Mittelfristig (3–12 Monate) - Strukturelle Implementierung
- [ ] Aufbau eines strukturierten ISMS nach BSI-Standard 200-2 / 200-3 (Strukturanalyse, Schutzbedarfsfeststellung und Risikoanalyse für IT und OT/CNC) (§ 30 BSIG)
- [ ] Umsetzung der technisch-organisatorischen Maßnahmen (z. B. Zugriffssteuerung, Netzwerksicherheit, regelmäßige Backup- und Wiederherstellungstests) (§ 30 BSIG)
- [ ] Etablierung eines formellen Lieferanten-Risikomanagements für externe Dienstleister und den Cloud-Backup-Anbieter (§ 30 BSIG)
- [ ] Ausarbeitung und Testung eines formellen Incident-Response- sowie Business-Continuity-Prozesses (BCM) (§§ 30, 32 BSIG)
- [ ] Durchführung der gesetzlich vorgeschriebenen Cybersicherheits-Schulung für die Geschäftsführung (§ 38 BSIG)

### 5.3 Langfristig (12–24 Monate)
- [ ] Abschluss komplexer OT- und Infrastrukturmaßnahmen (z. B. vollständige Netzwerksegmentierung der CNC-Produktion während geplanter Wartungsfenster) (§ 30 BSIG)
- [ ] Ausbau des Notfallmanagements zu einem vollständigen Business Continuity Management System (BCMS) nach BSI-Standard 200-4 (§ 30 BSIG)
- [ ] Durchführung regelmäßiger interner Audits, Management-Reviews und jährlicher Notfallübungen zur kontinuierlichen Verbesserung des ISMS (§§ 30, 38 BSIG)
- [ ] Prüfung einer formellen Zertifizierung ISO 27001 als Nachweis gegenüber Kunden und Geschäftspartnern

---

## 6. Offene Punkte / Rückfragen

Unternehmensverflechtungen: Bestehen Mutter-, Tochter-, Schwester- oder Partnerunternehmen, deren Beschäftigtenzahlen und Finanzkennzahlen bei der Einstufung berücksichtigt werden müssen?

Bilanzsumme: Wie hoch ist die zuletzt veröffentlichte Jahresbilanzsumme des Unternehmens?

---

*Erstellt von: ISB, Müller Maschinenbau GmbH*
*Datum: 10.11.2026*
*Version: 1.1*
