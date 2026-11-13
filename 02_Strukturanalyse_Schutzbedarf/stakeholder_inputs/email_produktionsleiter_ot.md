# E-Mail: Produktionsleiter → ISB | OT-Umgebung & CNC-Maschinen

**Von:** Markus Wagner (Produktionsleiter)  
**An:** ISB  
**Datum:** 13. November 2026  
**Betreff:** Re: Anfrage Produktionsumgebung – IT-Sicherheitsprojekt

---

Hallo,

ich sag's direkt: ich hab wenig Zeit für sowas, und meine Maschinen laufen seit 
Jahren ohne Probleme. Wenn jetzt jemand anfängt an der IT rumzuschrauben und die 
Produktion steht, dann ist das euer Problem, nicht meins.

Aber gut, hier was ich euch sagen kann:

**CNC-Maschinen (Fertigungshalle):**
- 6× CNC-Fräsmaschinen (Hersteller: verschiedene), Steuerung über proprietäre 
  Software, keine Netzwerkanbindung direkt – aber der MES-Server schickt die 
  Fertigungsaufträge
- 2× Schweißroboter (KUKA), Steuerung lokal, kein Fernzugriff

**MES:**
- Bosch Rexroth MES läuft auf SRV-MES-01
- Lieferant (Bosch Rexroth) verbindet sich 1–2× im Jahr remote für Wartung
  → läuft über normales Internet, kein VPN soweit ich weiß
- USB-Sticks werden für Datentransfer zwischen CNC und MES verwendet – hab ich 
  schon immer so gemacht, weil's schnell geht

**Verfügbarkeit:**
- Produktion läuft im 2-Schicht-Betrieb (06:00–22:00)
- Wartungsfenster: Samstag 06:00–10:00
- Stillstand kostet ca. 15.000–20.000 €/Stunde (Schätzung)

Ich will nicht dass jemand ohne meine Erlaubnis an den Maschinen oder am 
MES-Server rumspielt. Wenn da was geändert wird, dann nur mit mir zusammen und 
nur samstags früh.

Gruß  
Markus Wagner

---
*[ISB-Notiz: Remote-Wartung Bosch Rexroth ohne VPN → Red Flag, bestätigt Risiko; 
USB-Sticks unkontrolliert → Angriffsvektor Malware/Ransomware; Stillstandskosten 
15.000–20.000 €/h → Schutzbedarf hoch/sehr hoch für MES und Fertigungsprozess; 
Verfügbarkeitsfenster für Maßnahmen: Sa 06–10 Uhr]*
