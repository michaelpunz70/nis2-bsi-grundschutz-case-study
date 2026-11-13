# E-Mail: IT-Leiter → ISB | Inventar IT-Systeme & MES-Einbindung

**Von:** Klaus Hoffmann (IT-Leiter)  
**An:** ISB  
**Datum:** 15. Oktober 2026  
**Betreff:** Re: Anfrage Systemübersicht – Strukturanalyse

---

Hallo,

ich schick dir mal kurz was ich grad zur Hand habe. Für eine vollständige Liste 
bräuchte ich mehr Zeit – wir haben da nie wirklich eine saubere Dokumentation 
geführt.

**Server (On-Premise, Serverraum EG):**
- 1× Windows Server 2022 – Active Directory, DNS, DHCP (SRV-AD-01)
- 1× Windows Server 2019 – Dateiablage, Laufwerk Z: (SRV-FILE-01)
- 1× Windows Server 2022 – proAlpha ERP Applikationsserver (SRV-ERP-01)
- 1× Linux (Ubuntu 22.04) – Backup-Server, lokal + Sync zu CloudSecure (SRV-BKP-01)
- 1× Windows Server 2019 – MES-Server (SRV-MES-01) ← **der hängt auch im 
  Produktionsnetz, Hoffmann hat ihn mitverwaltet, aber der Prodleiter macht da 
  auch rum**

**Clients:**
- ca. 80 Windows 10/11 Workstations (Büro + Produktion)
- 15 Laptops (Vertrieb, mobil)
- kein MDM, kein zentrales Patch-Management

**Netzwerk:**
- 1× Cisco-Switch (unmanaged, Produktion) – kein VLAN, kein Netz-Trennung
- 1× Firewall (Sophos XG, Lizenz abgelaufen seit März 2026)
- WLAN: 2× AccessPoint, PSK-only, kein 802.1X

**Cloud / Extern:**
- Microsoft 365 (Exchange, Teams, SharePoint) – 148 Lizenzen
- CloudSecure GmbH – Backup-as-a-Service (Vertrag, kein SLA-Dokument vorhanden)
- DATEV – nur Datenexport aus proAlpha, läuft beim Steuerberater

**MES:**
Ja, das MES (Bosch Rexroth, Produktionsserver SRV-MES-01) ist über das normale 
Büronetz erreichbar. Wir haben das damals so gemacht weil's einfacher war. 
Ob das ein Problem ist frag den Produktionsleiter – der besteht darauf dass das 
so bleibt wegen der Wartung durch den Lieferanten.

Für Patch-Stand vom MES-Server hab ich keinen Überblick – das läuft autonom, 
Bosch Rexroth kommt einmal im Jahr vorbei.

Gruß  
Klaus

---
*[ISB-Notiz: Firewall-Lizenz abgelaufen → Sofortmaßnahme; MES ohne Netztrennung 
→ kritisches Risiko OT/IT; kein MDM → offener Punkt SYS; MES-Patch-Stand unbekannt 
→ offener Punkt für Risikoanalyse M4]*
