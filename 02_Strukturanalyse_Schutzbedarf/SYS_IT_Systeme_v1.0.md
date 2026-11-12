# IT- und OT-Systeme — Müller Maschinenbau GmbH

**Geltungsbereich:** Informationsverbund Müller Maschinenbau GmbH

---

| ID | System / Gruppe | Anzahl | Typ / Betriebssystem | Zugeordnete APP | Standort / Bemerkung |
|:---|:----------------|:-------|:---------------------|:----------------|:---------------------|
| **SYS&#8209;01** | Domain Controller (DC / AD) | 1 | Server / Windows Server 2019 | APP&#8209;06 | Serverraum (Annahme: physisch oder VM auf Hypervisor – offen) |
| **SYS&#8209;02** | Fileserver | 1 | Server / Windows Server 2019 | APP&#8209;07 | Serverraum (Annahme: physisch oder VM auf Hypervisor – offen) |
| **SYS&#8209;03** | ERP-Server (proAlpha) | 1 | Server / Windows Server 2022 | APP&#8209;01 | Serverraum (Annahme: physisch oder VM auf Hypervisor – offen) |
| **SYS&#8209;04** | Büro-PCs (Gruppe) | ca. 40 | Client / Windows 11 | APP&#8209;01, APP&#8209;02, APP&#8209;07 (DATEV nur auf Teilmenge) | Bürogebäude (Allgemeine Büro-Arbeitsplätze) |
| **SYS&#8209;04b** | CAD-Workstations (Gruppe) | ca. 5 (Annahme) | Client / Windows 11 (High-Performance GPU/RAM) | APP&#8209;01, APP&#8209;02, APP&#8209;03, APP&#8209;07 | Konstruktionsbüro (Höherer Schutzbedarf Vertraulichkeit) |
| **SYS&#8209;05** | Außendienst-Notebooks (Gruppe) | 8 | Client / Windows 11 (Annahme) | APP&#8209;01, APP&#8209;02, APP&#8209;07 | Mobil / Außendienst (Anbindung über VPN) |
| **SYS&#8209;06** | Firewall (FortiGate 60F) | 1 | Netzwerk / Sicherheitsappliance | Infrastruktur (alle netzbasierten APPs) | Serverraum (Zentrale Internet- und VPN-Anbindung; interne IT/OT-Segmentierung prüfen) |
| **SYS&#8209;07** | Switches & WLAN-Access-Points (Gruppe) | Mehrere | Netzwerk-Infrastruktur | Infrastruktur (alle netzbasierten APPs) | Bürogebäude & Konferenzräume (genaue Anzahl/Modelle offen) |
| **SYS&#8209;08** | MES-Rechner | 1 | OT-System / PC (OS offen) | APP&#8209;04 | Produktionshalle (Eigenständiger PC; hängt am gleichen Netz wie IT) |
| **SYS&#8209;09** | CNC-Maschinen & Bedienterminals (Gruppe) | 8 (6x Fräsen, 2x Drehen) | OT-Systeme / Industriesteuerung (OS offen) | APP&#8209;04 (indirekt) | Produktionshalle (Programmübernahme per USB-Stick; Netzwerkanbindung unklar) |
| **SYS&#8209;10** | USB-Sticks (Wechseldatenträger) | Mehrere | Speichermedien | – | Arbeitsvorbereitung / Produktion (Genutzt für Datentransfer APP&#8209;03 → SYS&#8209;09) |

## Hinweise

- **Hypervisor:** Falls SYS-01, SYS-02 und SYS-03 als VMs auf einem gemeinsamen Host laufen (z. B. VMware ESXi, Hyper-V), ist ein eigener Eintrag für den Virtualisierungshost erforderlich (Single Point of Failure).
- **Drucker/MFP & Smartphones:** Wurden in den Stakeholder-Emails nicht erwähnt; bei Bestätigung als SYS-11 / SYS-12 aufnehmen.

---

## Offene Fragen an Stakeholder

### 1. An den IT-Leiter (Jens Hoffmann)

- **Virtualisierung & Hardware (SYS-01 – SYS-03):** Handelt es sich bei unseren drei Servern (Domain Controller, Fileserver, proAlpha-ERP) um physische Einzelserver oder um virtuelle Maschinen (VMs) auf einem gemeinsamen Hypervisor (z. B. VMware ESXi / Hyper-V)?
- **CAD-Workstations (SYS-04b):** Wie viele CAD-Arbeitsplätze haben wir genau und verfügen diese über eine dedizierte Hardware-Ausstattung (High-Performance GPU/RAM) im Vergleich zu den normalen Büro-PCs?
- **Netzwerksegmentierung IT/OT (SYS-06 / SYS-08):** Sie erwähnten, dass das Produktionsnetz „irgendwie" am gleichen Netz hängt. Gibt es hierzu eine logische Trennung (VLANs, Firewall-Regeln auf der FortiGate) oder befinden sich Büro und Produktion im selben, ungetrennten Subnetz (Flat Network)?
- **WLAN & Mobile Geräte:** Gibt es neben den 45 Büro-PCs und 8 Notebooks auch Firmen-Smartphones/Tablets oder Netzwerkdrucker, die wir in der Systemliste erfassen müssen?
- **Endpoint Protection:** Welche Antiviren- bzw. EDR-Lösung setzen wir standardmäßig auf unseren Servern und Clients ein?

### 2. An den Produktionsleiter (Andreas Berger)

- **MES-Rechner (SYS-08):** Welches Betriebssystem läuft auf dem Rechner für das MES in der Produktion, und ist dieser Rechner in das Active Directory der IT eingebunden oder läuft er komplett autark?
- **CNC-Maschinen & Terminals (SYS-09):** Welches Betriebssystem oder welche Steuerungssoftware (z. B. Siemens Sinumerik, Fanuc o. ä.) läuft auf den Bedienterminals der 6 Fräsmaschinen und 2 Drehmaschinen? Haben diese Maschinen eine direkte Netzwerkanbindung oder laufen sie rein offline?
- **USB-Sticks (SYS-10):** Wie wird der Transport der Programme per USB-Stick von der Arbeitsvorbereitung zur Maschine organisiert (z. B. spezielle, verschlüsselte Firmen-Sticks oder handelsübliche USB-Sticks)? Gibt es eine Virenprüfung vor dem Einstecken an der CNC?

### 3. An den Konstruktionsleiter

- **CAD-Datenablage:** Wo werden die CAD/CAM-Daten der Konstruktion primär gespeichert – lokal auf den CAD-Workstations (SYS-04b), auf dem zentralen Windows-Fileserver (SYS-02) oder auf einem dedizierten CAD-Server?
