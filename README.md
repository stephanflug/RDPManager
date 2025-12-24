<div align="center">
<img width="974" height="509" alt="image" src="https://github.com/user-attachments/assets/477dd58e-f0e3-4034-895e-b398eec2a7b5" />

# RDPManager  
### Anwenderbeschreibung

Ein schlanker Verbindungsmanager für **Windows Remote Desktop (RDP)** – übersichtlich, schnell und sicher.

</div>

---

## Überblick

**RDPManager** speichert deine RDP-Ziele (**IP/Hostname**, **Benutzername**) in einer Liste und startet Verbindungen per Klick automatisch über den Windows-Remotedesktop-Client **mstsc.exe**.

---

## Features

✅ **Verbindungen verwalten**  
- RDP-Ziele anlegen, anzeigen und löschen

⚡ **Start per Doppelklick**  
- Verbindung direkt aus der Liste öffnen

🔐 **Sichere Passwortspeicherung**  
- Passwörter werden **nicht im Klartext** gespeichert  
- Ablage im **Windows Credential Manager (Anmeldeinformationsverwaltung)**

📦 **Export / Import (Backup & Umzug)**  
- Alle Verbindungen lassen sich als **verschlüsselte Exportdatei** sichern  
- Import auf einem anderen PC möglich (**Export-Passwort erforderlich**)

---

## Was wird gespeichert?

| Eintrag | Beschreibung | Beispiel |
|---|---|---|
| **Name** | frei wählbar | `Server Büro` |
| **Host/IP** | Zieladresse | `192.168.1.10` / `server.firma.local` |
| **Benutzername** | Login | `DOMAIN\user` / `user` |
| **Passwort** | Windows Credential Manager; beim Export zusätzlich verschlüsselt | *(nicht im Klartext sichtbar)* |

---

## Verbindung herstellen

So läuft der Verbindungsaufbau ab:

1. **RDPManager** stellt die benötigten **Anmeldedaten** im Windows-System bereit.  
2. Anschließend wird **mstsc.exe** mit dem Ziel gestartet.  
3. Die Anmeldung erfolgt mit den gespeicherten Daten *(abhängig von Richtlinien/Serverkonfiguration)*.

> Hinweis: Je nach Umgebung können zusätzliche Abfragen (z. B. Zertifikatswarnungen, MFA, Richtlinien) auftreten.

---

## Export / Import

### Export
- Erstellt eine Datei, z. B. `backup.rdpconfig`  
- Die Datei ist **verschlüsselt** und wird durch ein **Export-Passwort** geschützt  
- Ohne dieses Passwort ist die Datei **nicht entschlüsselbar**

### Import
- Stellt Verbindungen **inkl. Passwörter** wieder her

> **Wichtig:** Das Export-Passwort sicher aufbewahren.  
> Bei Verlust kann der Export **nicht wiederhergestellt** werden.

---

## Systemanforderungen

- **Windows 10 / 11**
- **Remote Desktop Client** ist Bestandteil von Windows (**mstsc.exe**)
- Für Verbindungen: **Netzwerkzugang** zum Zielsystem + **gültige Benutzerrechte**

---

## Sicherheitshinweise

- Keine unverschlüsselte Passwortablage in Dateien  
- Export-Sicherheit hängt maßgeblich von der Stärke des **Export-Passworts** ab  
- Empfehlung: **starkes Passwort** + Exportdatei **geschützt speichern**

---

### Unterstütze das Büro-Kaffeekonto!

Damit der Kaffee im Büro nie ausgeht, wäre eine kleine Spende super! 💰☕  
Jeder Beitrag hilft, die Kaffeemaschine am Laufen zu halten, damit wir alle produktiv bleiben können!

[**Spende für Kaffee**](https://www.paypal.com/donate/?business=ACU26RPTCA44S&no_recurring=0&item_name=Dieses+Projekt+und+der+Service+kann+nur+durch+eure+Spenden+finanziert+werden.&currency_code=EUR)

Vielen Dank für deine Unterstützung! 🙌
