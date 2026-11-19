# HOLMER Montage-QM-Portal

Internes Qualitätsmanagement-Portal für die Endmontage von HOLMER Maschinen.
Die Anwendung ist als Single-File-Web-Portal umgesetzt – ohne Build-Prozess,
ohne externe Abhängigkeiten und ohne Server-Backend.

## Funktionsumfang

- **Dashboard** – Kennzahlen (offene Prüfaufträge, offene Fehlermeldungen,
  laufende 8D-Prozesse, Abnahmequote) und Statusübersicht je Montagestation.
- **Prüfaufträge** – Anlegen, filtern und abarbeiten von Prüfaufträgen je
  Maschine/Baunummer und Montagestation mit Prüfschritten.
- **Checklisten** – Stationsbezogene Montage-Checklisten mit Fortschritt,
  speicherbar je Baunummer.
- **Fehlermanagement & 8D** – Erfassung von Fehlermeldungen nach Schweregrad
  und vollständiger 8D-Report (D1–D8) je Fehler.

Alle Eingaben werden lokal im Browser (localStorage) gespeichert.
Beispieldaten dienen der Demonstration und können jederzeit zurückgesetzt
werden.

## Nutzung

Die Datei `index.html` direkt im Browser öffnen – mehr ist nicht nötig.

Alternativ als statische Site ausliefern (z. B. GitHub Pages, nginx, IIS):

```bash
# einfacher Testserver (optional)
python3 -m http.server 8080
# danach http://localhost:8080 öffnen
```

## Projektstruktur

```
index.html              Portal (noch PR: Feature-Branch)
docs/
  ANFORDERUNGEN.md      Anforderungen und Prozessbeschreibung QM-Portal
```

## Hinweis

Demonstrations- und Beispieldaten repräsentieren keine realen Maschinen- oder
Personendaten. Für den produktiven Betrieb mit mehreren Nutzern wäre ein
Backend mit Authentifizierung und zentraler Datenaufbewahrung zu ergänzen.
