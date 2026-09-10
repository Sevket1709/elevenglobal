# Eleven Global – bearbeitbares Website-Mockup

## Stand und Quellen

Rekonstruktion des PDF-Mockups `Eleven_Global_Webseiten-Mockup_2026-09-08.pdf` (Website-Version 6) plus `LASTENHEFT.md`. Kein Zugriff auf den ursprünglichen Quellcode. Bestehende Live-Website nicht verändert.

Deutsch ist die Referenzsprache. Englische und türkische Texte wurden für dieses Mockup neu übersetzt. Nicht sichtbare Akkordeon- und Markttexte wurden als Entwurf ergänzt. Rechtstexte sind aus den sichtbaren PDF-Seiten übertragen, nicht juristisch geprüft; weitere nicht sichtbare Abschnitte dürfen nicht als vollständig rekonstruiert gelten. Bilddateien wurden verlustfrei aus den PDF-Screenshots extrahiert; die Gestaltung zeigt die Bildausschnitte über CSS. Für den Produktivbetrieb werden die ursprünglichen Einzelbilder benötigt.

## Dateien und Start

- `dist/index.html`: Grundgerüst und Bearbeitungsdialoge.
- `dist/app.js`: Navigation, Formular-Demo, Texteditor, Import und Export, lokale Zustandsspeicherung.
- `dist/content.js`: Inhalte DE/EN/TR sowie deutsche Referenz-Rechtstexte.
- `dist/style.css`: responsive Gestaltung und Farbvariablen.
- `dist/impressum/index.html`, `dist/datenschutz/index.html`, `dist/agb/index.html`: eigenständige URL-Einstiegspunkte.
- `LASTENHEFT.md`: übernommene fachliche Projektgrundlage.

Statische Website ohne Paketinstallation oder Build. Mit einem beliebigen statischen HTTP-Server aus `dist/` bereitstellen. Dateien nicht über `file://` öffnen, da ES-Module einen HTTP-Kontext benötigen. Syntaxprüfung: `node --check dist/app.js` und `node --check dist/content.js`.

## Bearbeiten

Oben „Texte bearbeiten“ aktivieren, dann einen umrandeten Text anklicken. Unter „Entwurf & Export“ Akzentfarbe und Umsetzungsnotizen ändern. Änderungen bleiben ausschließlich im aktuellen Browser. „Entwurf exportieren“ erzeugt eine JSON-Datei zum Teilen mit ChatGPT oder Codex. Diese lokalen Änderungen verändern weder den veröffentlichten Projektquellcode noch GitHub automatisch.

Der JSON-Export enthält `overrides` je Sprache. Codex soll Änderungen daraus nach Prüfung in `content.js` bzw. `style.css` übernehmen. Der Import validiert bekannte Schlüssel und schreibt Texte ausschließlich als Textknoten, nicht als HTML.

## Verbindliche Grenzen

- Kontaktformular prüft nur Eingaben. Kein Versand, keine serverseitige Speicherung, keine echte Mail-Integration.
- Keine FIFA-Lizenzbehauptungen und keine erfundenen Referenzen oder Spieler.
- Rechtstexte und Leistungsumfang vor öffentlichem Echtbetrieb fachlich/rechtlich prüfen.
- Backend, Recherche/Crawler, Akquise, Rollen und Spielerdossiers sind spätere Ausbaustufen.
- Benutzerdefinierte Änderungen, Sprache und Notizen nur in localStorage; Formularinhalte werden nicht gespeichert.

## Gemeinsamer Workflow mit Codex und GitHub

1. Ein gemeinsames privates GitHub-Repository als verbindlichen Quellstand wählen.
2. Diesen Projektstand einmalig dorthin übernehmen; die aktuelle Sites-Verknüpfung ist kein GitHub-Repository.
3. `main` enthält den abgestimmten Stand. Pro Aufgabe einen Branch verwenden, z. B. `design/contact-layout` oder `feature/contact-mail`.
4. UI-/Inhaltstexte und technische Features als getrennte Aufgaben bearbeiten. Nicht parallel dieselben Dateien ohne Abstimmung verändern.
5. Änderungen als Pull Request prüfen, zusammenführen und den nächsten Arbeitsstand von `main` beginnen.
6. Exportierte Mockup-JSON-Dateien explizit übergeben; keine automatische Synchronisation behaupten.

Für Mailversand werden Anbieter/Versandmethode, konfigurierter Secret-Zugang und die Bestätigung eines aktiven Postfachs benötigt. Zugangsdaten niemals im Chat oder Repository hinterlegen. Echte Testnachrichten erst nach ausdrücklicher Autorisierung versenden.

## Prüfung dieses Stands

Statische Prüfungen: JS-Syntax, lokale Asset-/Routenreferenzen, Sprachschlüssel und HTML-Struktur. Kein Browser-/End-to-End-Test beauftragt. WebMCP wird optional nach Fähigkeit des Browsers registriert; Validierung in unterstütztem Browserkontext war nicht verfügbar.
