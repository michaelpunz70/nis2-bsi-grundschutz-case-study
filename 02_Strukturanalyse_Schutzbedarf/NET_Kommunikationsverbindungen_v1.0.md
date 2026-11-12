# Kommunikationsverbindungen — Müller Maschinenbau GmbH

**Geltungsbereich:** Informationsverbund Müller Maschinenbau GmbH

---

| ID | Verbindung / Strecke | Typ / Protokoll | Zugeordnete SYS / APP | Beschreibung / Zweck | Sicherheitsaspekt / Bemerkung |
|:---|:---------------------|:----------------|:-----------------------|:---------------------|:------------------------------|
| **NET&#8209;01** | Büro-LAN (Clients → Server) | Lokal / Ethernet (TCP/IP) | SYS&#8209;04, SYS&#8209;04b ↔ SYS&#8209;01, SYS&#8209;02, SYS&#8209;03 | Zugriff der Büro- und CAD-PCs auf Active Directory, Fileserver und proAlpha ERP | Standard-Unternehmensnetzwerk (Admin- & Büro-Bereich) |
| **NET&#8209;02** | Produktions-Netz / Übergang | Lokal / Ethernet / WLAN (unklar) | SYS&#8209;08, SYS&#8209;09 ↔ SYS&#8209;07 (gemeinsames LAN mit SYS&#8209;01..SYS&#8209;04) | Anbindung des MES-Rechners und ggf. CNC-Terminals | Kritisch: Hängt im selben Netz wie das Büro (Flat Network). FortiGate (SYS&#8209;06) filtert nur am Internet-Perimeter, nicht zwischen IT und OT. |
| **NET&#8209;03** | Internet-Anbindung (Zentral) | Extern / Glasfaser/DSL über FortiGate | SYS&#8209;06 → Internet | Zentraler Internet-Zugang für E-Mail, Web-Browsing und Updates | Gesichert durch Firewall (FortiGate 60F) |
| **NET&#8209;04** | Außendienst-VPN | Extern / Verschlüsseltes VPN | SYS&#8209;05 → SYS&#8209;06 | Sichere Einwahl der 8 Außendienst-Notebooks ins Firmennetz | Endpunkt-Anbindung über FortiGate |
| **NET&#8209;05a** | Microsoft 365 (SaaS) | Extern / HTTPS (TLS) | SYS&#8209;04, SYS&#8209;04b, SYS&#8209;05 → Microsoft Cloud (APP&#8209;02) | Kommunikation der Büro- und Außendienst-Clients mit Exchange Online, SharePoint, Teams, OneDrive | Verschlüsselter Cloud-Traffic über Internet (Benutzerauthentifizierung) |
| **NET&#8209;05b** | CloudSecure Backup-Tunnel | Extern / Verschlüsseltes VPN | SYS&#8209;01, SYS&#8209;02, SYS&#8209;03 → CloudSecure GmbH (APP&#8209;08) | Tägliche, automatisierte Datensicherung der Server über dedizierten VPN-Tunnel | Kritischer Infrastruktur-Kanal zum externen Dienstleister (Supply-Chain-Risiko) |
| **NET&#8209;06** | USB-Wechseldatenträger (Offline-Kanal) | Physisch / Offline | SYS&#8209;10 zwischen SYS&#8209;04b (AV) und SYS&#8209;09 (CNC) | Transport von CNC-Programmen von der Arbeitsvorbereitung direkt an die Maschinen | Kritisch: Kein netzbasierter Kanal, physische Übertragung (Risiko von Malware-Einschleppung) |
| **NET&#8209;07** | WLAN-Zugang (Büro / Konferenz) | Funk / Wi-Fi (WPA2/WPA3) | SYS&#8209;07 ↔ Mobile Clients / AP-Gruppe | Kabelloser Netzwerkzugang für interne Mitarbeiter und Gäste in den Räumlichkeiten | Segmentierung (Gäste- vs. Firmen-WLAN) muss geprüft werden |

## Offene Fragen an den IT-Leiter (Jens Hoffmann)

- **Netzsegmentierung (NET-02):** Gibt es zwischen dem Büro-Netz und dem Produktions-Netz dezidierte VLANs oder Firewall-Regeln auf der FortiGate, oder sind beide Bereiche technisch im selben unsegmentierten Subnetz (Flat Network) verbunden?
- **WLAN-Sicherheit (NET-07):** Befinden sich die WLAN-Geräte (in Büro und Konferenzräumen) im internen Firmennetz oder gibt es ein separates, isoliertes Gäste-WLAN?
- **Fernwartung (Remote Maintenance):** Gibt es für die CNC-Fräsmaschinen oder das MES eine temporäre Fernwartung (z. B. per TeamViewer oder direktem VPN durch den Maschinenhersteller)? Falls ja, wird eine eigene NET-Verbindung erfasst.
