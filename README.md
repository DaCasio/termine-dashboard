# 🛰️ Termin Monitor - Orbital Control

![Version](https://img.shields.io/badge/Version-2.5-00cae3.svg)
![License](https://img.shields.io/badge/License-Private-ff4d4d.svg)

Ein hochmoderner, browserbasierter Termin-Planer mit orbitalem Design und direkter Cloud-Synchronisation via GitHub API.

---

## 🚀 Kernfunktionen / Core Features

### 🇩🇪 Deutsch
* **Echtzeit-Synchronisation:** Speichert Daten direkt in deinem GitHub-Repo als `termine.json`.
* **Intelligentes Filtersystem:** Automatische "LIVE NOW" Erkennung und Filterung nach Tags (Kategorien).
* **Dynamische Suche:** Echtzeit-Suche über alle Titel, Notizen und Checkboxen.
* **Präzisions-Countdown:** Live-Anzeige der verbleibenden Zeit bis zum Start oder Ende.
* **Markdown & Checkboxen:** Unterstützt Fett-Text, Farben und interaktive Aufgabenlisten.
* **ICS-Import:** Importiert Termine direkt aus Kalender-Dateien.

### 🇺🇸 English
* **Real-Time Sync:** Saves data directly to your GitHub repo as `termine.json`.
* **Smart Filtering:** Automatic "LIVE NOW" detection and tag-based categorization.
* **Dynamic Search:** Real-time search across all titles, notes, and checkboxes.
* **Precision Countdown:** Live display of remaining time until start or expiration.
* **Markdown & Checkboxes:** Supports bold text, colors, and interactive to-do lists.
* **ICS Import:** Import appointments directly from calendar files.

---

## 🛠️ Technische Einrichtung / Setup Instructions

### 1. GitHub Repository
* Erstelle ein **privates** Repository (z.B. `info-board`).
* Erstelle eine leere Datei namens `termine.json` mit folgendem Inhalt: `[]`.

### 2. GitHub Token (PAT)
* Gehe zu **Settings > Developer Settings > Personal Access Tokens (classic)**.
* Erstelle ein neues Token mit dem Scope `repo`.
* Teile das Token in zwei Hälften auf und trage sie in die Variablen `t1` und `t2` im Code ein (um automatische Scans durch GitHub zu erschweren).

### 3. API URL
* Passe die `G_URL` im Script-Teil an: 
  `https://api.github.com/repos/DEIN_NUTZERNAME/DEIN_REPO/contents/termine.json`

### 4. PIN Schutz
* Der Standard-PIN ist `0508`. 
* Um den PIN zu ändern, generiere einen neuen Base64-String deines PINs und ersetze den Wert in `P_ENC`.

---

## 📖 Bedienung / How to Use

| Aktion | Beschreibung |
| :--- | :--- |
| **Speichern** | Titel und Enddatum sind Pflichtfelder. |
| **Suchen** | Nutze das Suchfeld, um Inhalte sofort zu filtern. |
| **Formatierung** | Nutze die Toolbar für **B** (Fett), **S** (Durchgestrichen) oder Farben. |
| **Checklisten** | Klicke auf `+ CHECKBOX` im Editor oder direkt auf die Box in der Kartenansicht. |
| **Archivieren** | Füge das Tag `ARCHIV` hinzu, um einen Termin aus der Hauptliste zu entfernen. |

---

## 🔒 Sicherheitshinweis / Security Note
Da dieses Tool Client-seitig im Browser läuft und das GitHub-Token im Quellcode enthält, sollte die HTML-Datei **niemals in einem öffentlichen Repository** hochgeladen werden. Nutze es lokal oder hoste es in einer privaten, passwortgeschützten Umgebung.

---
*Developed for Orbital Control Systems. Status: Operational.*
