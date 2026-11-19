# Anforderungen: HOLMER Montage-QM-Portal

## Zielsetzung

Digitale Abbildung des Qualitätsmanagements in der Endmontage. Das Portal
ersetzt papiergebundene Prüflisten und Excel-Fehlerverfolgung und schafft
eine durchgängige Historie je Maschine (Baunummer).

## Prozesse

### 1. Prüfaufträge
- Je Maschinen-Konfiguration wird beim Anlauf der Endmontage ein Prüfauftrag
  angelegt (Maschine, Baunummer, Station, Verantwortlich, Fälligkeit).
- Der Auftrag enthält Prüfschritte je Montagestation.
- Status: Offen → In Arbeit → Abgeschlossen; Blockiert bei hängendem Fehler.

### 2. Checklisten je Montagestation
- Vorbereitung / Fahrwerk, Hubwerk, Kabine, Elektrik & Hydraulik,
  Reinigung & Schutzvorrichtungen, Endabnahme.
- Jeder Punkt wird je Baunummer abgehakt; Fortschritt wird angezeigt.
- Wird ein Punkt als fehlerhaft markiert, kann direkt eine Fehlermeldung
  erzeugt werden.

### 3. Fehlermanagement & 8D
- Fehlermeldung mit Schweregrad (Kritisch / Major / Minor), Station,
  kurzfristiger Sofortmaßnahme und Ursachenvermutung.
- Kritische Fehler durchlaufen einen 8D-Report (D1–D8):
  1. Team bilden
  2. Problembeschreibung
  3. Sofortmaßnahmen
  4. Ursachenanalyse (5-Why / Ishikawa)
  5. Korrekturmaßnahmen
  6. Wirksamkeit nachweisen
  7. Präventive Maßnahmen (Lessons Learned)
  8. Team-Anerkennung / Abschluss

## Nichtfunktionale Anforderungen

- Single-File-Anwendung ohne Backend; Betrieb im Werkstatt-Umfeld auch auf
  Tablets.
- Datenhaltung clientseitig (localStorage); Export als JSON möglich.
- Deutschsprachige Oberfläche, min. WCAG-AA-Kontraste für Shopfloor-Displays.

## Umsetzung

Aktuelle Umsetzung: statisches Portal (`index.html`) mit Beispieldaten.
Geplante Ausbaustufen: Mehrbenutzerbetrieb, Backend mit Datenbank,
Upload von Fotos und Erkannt-Erkundungsschritt je Prüfschritt.
