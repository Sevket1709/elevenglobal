# Eleven Global

Arbeitsstand für die gemeinsame Weiterentwicklung mit Codex. Das Repository enthält das bearbeitbare Website-Mockup und das fortgeschriebene Lastenheft für das geplante interne Backend.

## Website-Mockup

Das Mockup ist eine statische Website unter `dist/` und benötigt keinen Build-Schritt.

```bash
python3 -m http.server 8000 --directory dist
```

Danach: `http://localhost:8000`

Es umfasst:

- Startseite in Deutsch, Englisch und Türkisch
- bearbeitbare Texte, Akzentfarbe, Notizen sowie JSON-Import/-Export
- Leistungen, Märkte, Kontaktformular-Demo
- separate Einstiegspunkte für Impressum, Datenschutz und AGB
- responsive Gestaltung nach dem gelieferten PDF-Mockup

Das Kontaktformular versendet keine E-Mail. Browseränderungen landen nur in `localStorage` und müssen per JSON exportiert oder von Codex in den Quellcode übernommen werden.

Weitere Hinweise: [`docs/MOCKUP.md`](docs/MOCKUP.md)

## Backend-Planung

Das verbindliche Arbeitsdokument liegt in [`LASTENHEFT.md`](LASTENHEFT.md). Abschnitt 8 beschreibt:

- Auswahl ausschließlich bei **vereinslos UND nachweislich ohne Berater**
- Spielerübersicht und manuelle Prüfliste
- Vereins-, Marktwert- und Quellenhistorien
- internes PDF-Exposé sowie persönlich freigegebene Vereinsfassung
- Datenmodell, Rollen, Nachvollziehbarkeit und Abnahmetests
- stufenweise Codex-Umsetzung mit synthetischen Testdaten

Transfermarkt und FotMob sind als gewünschte Quellen spezifiziert. Live-Crawler bleiben deaktiviert, bis Nutzungsrechte, erlaubte Felder, Abrufweg, Frequenz, Speicherung und externe PDF-Weitergabe schriftlich geklärt sind. FotMob untersagt automatisches/systematisches Auslesen ohne ausdrückliche Zustimmung.

## Empfohlener Codex-Start

1. Repository in Codex als Umgebung auswählen.
2. `README.md`, `LASTENHEFT.md` und `docs/MOCKUP.md` lesen.
3. Mit Meilenstein **M1** aus Abschnitt 8.10 beginnen: Datenmodell, synthetischer Import, UND-Logik und Testfälle.
4. Für jedes Arbeitspaket einen eigenen Branch und Pull Request verwenden.
5. Keine produktiven Spielerdaten, PDFs, Zugangsdaten oder API-Schlüssel einchecken.

Noch nicht umgesetzt sind Backend, Anmeldung, Datenbank, PDF-Generator, Live-Crawler und echter Kontaktversand.
