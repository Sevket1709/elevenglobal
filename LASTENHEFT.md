# Eleven Global – Lastenheft (Arbeitsstand)

**Stand:** 10. September 2026  
**Version:** 0.2 – Backend und Spielerexposé  
**Status:** Fortlaufendes Arbeitsdokument; neue Anforderungen spezifiziert, noch nicht implementiert oder abgenommen.  
**Grundsatz:** Website und Backend dürfen nach dem neuen Auftrag parallel weiterentwickelt werden. Aktueller Schwerpunkt ist das Lastenheft für Spielerrecherche, Übersicht und CI-PDF. Der automatische Live-Datenabruf setzt geklärte Nutzungsrechte voraus. Die Website-Offenpunkte bleiben bestehen.

**Verbindlichkeit:** Ausdrückliche Nutzeranforderungen sind als Anforderungen formuliert. Mit „Vorschlag“ markierte Werte und Entscheidungen benötigen noch Freigabe. Die Aktualisierung in Abschnitt 8 konkretisiert und ersetzt entgegenstehende ältere Festlegungen, insbesondere ODER-Filter und spätere Priorisierung des PDFs.

## 1. Projektziel

Eleven Global soll eine professionelle, mehrsprachige Website sowie ein internes Backend für die strukturierte Recherche, Bewertung und persönliche Ansprache potenziell relevanter Fußballspieler erhalten. In einer späteren Ausbaustufe soll das System außerdem vereinsgerechte Spielerunterlagen für die gezielte Ansprache von Clubs erzeugen.

## 2. Aufgabenreihenfolge

1. Backend-MVP und CI-Spielerexposé spezifizieren und abstimmen (aktueller Auftrag)
2. Ziel-Repository und Datenrechte klären; Startregionen und Suchumfang festlegen
3. Backend mit Übersicht, Spielerprofilen und PDF-Prozess zunächst anhand synthetischer oder freigegebener Daten entwickeln
4. Freigegebene Quellen anbinden und wiederkehrende Datenübernahme aktivieren
5. Datenqualität, persönliche Prüfung, PDF-Export und Betrieb abnehmen
6. Parallel: Website vollständig fertigstellen, Kontaktformular technisch anbinden und real testen; Inhalte, Responsivität und Sprachfassungen prüfen
7. Später: Akquise-Kommunikation per E-Mail/WhatsApp und personalisierte Nachrichten mit persönlicher Freigabe entwickeln

## 3. Website – aktueller Stand

### 3.1 Umgesetzt

- Mehrsprachige Unternehmenswebsite
- Eigenständige Seiten für Impressum, Datenschutz und Allgemeine Geschäftsbedingungen
- Verlinkung der Rechtstexte im Footer
- Impressum für „Eleven Global, eine Marke der STARKS Betriebs GmbH“
- Kontaktangaben: contact@eleven-global.com und 0178 639 4229
- Geschäftsführer: Sevket Baykurd
- Entfernung öffentlicher Hinweise auf eine noch nicht erteilte FIFA-Fußballagentenlizenz

### 3.2 Noch offen

- Kontaktformular mit dem tatsächlichen Postfach verbinden
- Versand und Zustellung von Testanfragen prüfen
- Abschließende Prüfung aller Inhalte, Links, Darstellungen und Sprachfassungen
- Finale Freigabe der Website

### 3.3 Bearbeitbares Mockup im aktuellen Arbeitskontext

Am 10. September 2026 wurde eine eigenständige bearbeitbare Rekonstruktion anhand des PDF-Übergabestands erstellt: https://eleven-global-mockup.starks-resta-8168.chatgpt.site. Sie ist nicht der Originalquellcode der vorherigen Website. Text-/Farbänderungen werden dort nur im jeweiligen Browser gespeichert und können als JSON exportiert werden. Das Kontaktformular ist eine Demo ohne Versand. Das Backend soll diese lokale Mockup-Speicherung nicht als produktive Datenhaltung übernehmen.

## 4. Backend und Spielerrecherche – vorgesehener Umfang

- Webseiten anhand definierter Suchparameter recherchieren beziehungsweise crawlen
- Im Backend-MVP Spieler identifizieren, die gleichzeitig vereinslos UND ohne Berater sind; unklare Angaben gesondert prüfen, siehe Abschnitt 8.2
- Gefundene Daten mit Quellen und Prüfdatum dokumentieren
- Zu jedem Spieler eine kompakte Entscheidungszusammenfassung mit den wichtigsten Eckdaten bereitstellen
- Relevante Kontaktmöglichkeiten wie E-Mail und – soweit rechtmäßig verfügbar – Telefonnummer beziehungsweise WhatsApp erfassen
- Spieler einzeln über Checkboxen für E-Mail und/oder WhatsApp persönlich freigeben
- Ohne persönliche Freigabe darf keine Nachricht versendet werden
- Versandstatus, Zeitpunkt, Kanal, verwendete Nachricht und verantwortlichen Nutzer protokollieren
- Datenschutz, Einwilligungen, Kontaktgrundlage, Plattformregeln und Widersprüche müssen vor der Umsetzung rechtlich und technisch geprüft werden

## 5. Personalisierte Akquise – vorgesehener Umfang

- Zielgerichtete, persönliche Nachricht pro Empfänger statt generischer Massenansprache
- Nutzung ausschließlich geprüfter Spielerdaten und Quellen
- Unterschiedliche Vorlagen für Spieler, Ansprechpartner und Vereine
- Erstellung eines eigenen Skills für Recherche-Zusammenfassung, Relevanzbewertung und Formulierung
- Menschliche Prüfung und Freigabe vor jedem Versand
- Sprachvarianten zunächst Deutsch, Englisch und Türkisch

## 6. Strukturiertes PDF-Spielerdossier für Vereine

**Status:** Bestandteil des aktuellen Backend-MVP; noch nicht implementiert  
**Zeitpunkt:** Zusammen mit Übersicht und Spielerprofilen nach Abstimmung des Datenmodells; ohne Abhängigkeit von der Fertigstellung der Website  
**Ziel:** Ein Skript erzeugt aus geprüften Spielerdaten ein professionelles PDF, das für die persönliche Ansprache und Entscheidungsunterstützung von Vereinen genutzt werden kann.

### 6.1 Voraussichtliche Inhalte des Dossiers

- Name, Geburtsdatum beziehungsweise Alter und Nationalität(en)
- Pass- und gegebenenfalls Spielberechtigungsinformationen
- Hauptposition, Nebenpositionen, bevorzugter Fuß und Körpergröße
- Aktueller beziehungsweise letzter Verein und Liga
- Vertragsstatus, Vertragsende und Verfügbarkeit
- Mögliche Transferart und bekannte wirtschaftliche Rahmenbedingungen
- Leistungsdaten der aktuellen und relevanten vergangenen Spielzeiten
- Positionsbezogene Kennzahlen, Einsatzminuten und Startelfeinsätze
- Spielprofil, Stärken, Entwicklungsfelder und besondere Merkmale
- Verletzungs- und Verfügbarkeitsinformationen, jeweils mit Quelle und Stand
- Links zu Highlight-Videos und möglichst zu vollständigen Spielen
- Begründung der sportlichen und wirtschaftlichen Eignung für den konkreten Empfängerverein
- Relevante Registrierungs- oder Ausländerregelungen, soweit geprüft
- Kontakt- und Vertretungsstatus sowie interne Freigabe
- Quellenverzeichnis, Prüfdatum und Kennzeichnung der Datenqualität
- Eleven-Global-Kontaktdaten und klare Handlungsaufforderung

### 6.2 Anforderungen an das spätere Skript

- Eingabe aus einem freigegebenen Spielerprofil im Backend
- Erzeugung eines einheitlich gestalteten, druckfähigen PDFs
- Konfigurierbare Markenfarben, Logo, Bilder und Kontaktdaten
- Sprachvarianten mindestens Deutsch und Englisch; Türkisch nach Bedarf
- Empfängerbezogene Anpassung der Vereinsansprache
- Versionsnummer, Erstellungszeitpunkt und interner Dokumentstatus
- Klare Trennung zwischen verifizierten Fakten, Einschätzungen und offenen Angaben
- Fehlende Werte dürfen nicht erfunden werden und müssen eindeutig gekennzeichnet oder ausgelassen werden
- Nur rechtmäßig nutzbare Fotos, Statistiken, Videos und Quellen dürfen veröffentlicht werden
- Vorschau und persönliche Freigabe vor Export oder Versand
- Protokollierung der erzeugten und versendeten Version

### 6.3 Abnahmekriterien für die spätere Umsetzung

- Das PDF wird aus einem vollständigen Testprofil fehlerfrei erzeugt
- Alle sichtbaren Angaben stimmen mit dem freigegebenen Backend-Datensatz überein
- Quellen und Datenstand sind nachvollziehbar
- Fehlende Angaben führen nicht zu erfundenen Inhalten oder Layoutfehlern
- Das Dokument ist auf Desktop, Mobilgerät und im Ausdruck gut lesbar
- Der Export wird erst nach persönlicher Freigabe ermöglicht
- Eine versendete Version bleibt revisionssicher nachvollziehbar

### 6.4 Rückfragen, die vor Beginn dieses Tasks gemeinsam zu klären sind

1. Welche Vereinsarten und Ligen sollen zuerst angesprochen werden?
2. Soll das Dossier kurz und vertrieblich oder ausführlich und scoutingorientiert sein?
3. Wie viele Seiten soll die Standardversion umfassen?
4. Welche Statistikquellen dürfen technisch und lizenzrechtlich genutzt werden?
5. Welche wirtschaftlichen Angaben sollen Vereine sehen?
6. Soll pro Spieler nur ein Dossier oder je Empfängerverein eine angepasste Variante entstehen?
7. Welche Fotos, Videoquellen und Markenassets liegen mit Nutzungsrechten vor?
8. Wer darf Dossiers erstellen, prüfen, freigeben und versenden?
9. Soll später zusätzlich ein Spieler-Vergleichsdossier unterstützt werden?

## 7. Nächster unmittelbar zu bearbeitender Task

Das Backend-Lastenheft in Abschnitt 8 abstimmen, das gemeinsame GitHub-Repository bestimmen und ein erstes Umsetzungspaket für Datenmodell, Spielerübersicht und PDF-Entwurf daraus ableiten. Noch kein Crawler, wiederkehrender Job oder Nachrichtenversand ist aktiviert.

Der frühere Website-Task bleibt separat offen: Kontaktformular mit **contact@eleven-global.com** verbinden und nach Freigabe real testen. Dafür fehlen E-Mail-Anbieter beziehungsweise Versandmethode und die Bestätigung eines aktiven Postfachs.

## 8. Backend-MVP: Spielerübersicht und CI-Exposé

### 8.1 Ziel, Nutzen und Abgrenzung

**Ziel:** Eleven Global erhält einen geschützten internen Arbeitsbereich, in dem passende Spieler recherchiert, eingeordnet, persönlich geprüft und für eine mögliche Vereinsansprache aufbereitet werden. Eine Übersicht beantwortet: Wer ist verfügbar, wer hat keinen Berater, welche Laufbahn und welchen belegten Marktwert hat der Spieler, und ist sein Exposé aktuell und freigegeben?

**Vom Nutzer festgelegt:**

- Transfermarkt und FotMob als gewünschte regelmäßig zu aktualisierende Datenquellen.
- Für die erste Version gilt die zuletzt ausdrücklich genannte UND-Bedingung: vereinslos UND ohne Berater.
- Spielerübersicht mit Einordnung anhand bisheriger Vereine, Marktwert und Historie.
- Für jeden aufgenommenen passenden Spieler ein PDF-Exposé in der Eleven-Global-CI.
- Nutzung sowohl für interne Bewertung als auch als Grundlage für die spätere Vereinsansprache.

**MVP-Bestandteile:** geschützter Zugang, konfigurierbare Quellenübernahme, Identitätsabgleich, Statusprüfung, Spielerübersicht, Detailprofil, nachvollziehbare Historien, CI-PDF-Erzeugung, Prüf-/Freigabeablauf und Betriebsübersicht.

**Nicht Teil des MVP:** automatischer E-Mail-/WhatsApp-Versand, Massenakquise, öffentliche Spielerdatenbank, Vertragsabschluss, automatisches Scouting-Ranking, automatische Darstellung eines Vertretungsmandats und Verarbeitung von Gesundheitsdaten. Eine konkrete Zuordnung zu einem Empfängerverein ist eine spätere Erweiterung, kein Muss für das erste allgemeine Exposé.

### 8.2 Zielgruppe und eindeutige Filterlogik

**BE-001 – Positive Kriterien:** Ein Spieler gehört nur dann in die Standardansicht „Passende Spieler“, wenn beide Statusangaben ausdrücklich belegt, aktuell und widerspruchsfrei sind. Ein ausgefüllter Beratername ist ein negatives Kriterium; ein fehlender Eintrag ist kein positiver Nachweis.

| Vereinsstatus | Beraterstatus | Ergebnis im MVP |
| --- | --- | --- |
| Nachweislich vereinslos | Nachweislich ohne Berater | Passender Spieler |
| Nachweislich vereinslos | Berater vorhanden | Nicht passend |
| Bei einem Verein | Ohne Berater | Nicht passend |
| Nachweislich vereinslos | Unbekannt / keine Angabe | Prüfliste, nicht als Treffer zählen |
| Unbekannt / keine Angabe | Ohne Berater | Prüfliste, nicht als Treffer zählen |
| Widersprüchlich oder veraltet | Beliebig | Prüfliste bis zur erneuten Klärung |

**BE-002 – Bedeutung des Vereinsstatus:** „Ablösefrei“, auslaufender Vertrag, Leihe, fehlender Kaderplatz, Verletzung oder fehlender Datensatz dürfen nicht automatisch in „vereinslos“ übersetzt werden. Karriereende wird separat geführt und nicht als aktive Vereinslosigkeit behandelt. „Vereinslos seit“ wird nur angegeben, wenn ein belegtes Datum vorliegt; ansonsten bleibt es unbekannt.

**BE-003 – Bedeutung des Beraterstatus:** Ein Strich, leeres Feld, ausgeblendete Information oder eine nicht gefundene Profilseite ergibt „unbekannt“. Selbstvertretung, Familienvertretung und ein auslaufendes Mandat bleiben eigene Prüfzustände, bis die fachliche Einordnung geklärt ist. „Ohne Berater“ setzt eine ausdrückliche Quellenangabe oder dokumentierte persönliche Bestätigung voraus; auch Quellenangaben sind keine Gewähr für die rechtliche Vertretungssituation.

**BE-004 – Nachweis:** Vereins- und Beraterstatus erhalten jeweils Quelle, Belegtext beziehungsweise zulässige Referenz, sachlichen Datenstand, Abrufzeit, Prüfperson und Prüfzeit. Angaben ohne diese Mindestnachweise bleiben in der Prüfliste. Eine manuell bestätigte Angabe wird durch einen Folgeimport nicht stillschweigend überschrieben.

**Vorschlag zur Aktualität:** Quellprüfung mindestens täglich; kritische Statusbelege nach sieben Tagen ohne erfolgreiche Aktualisierung als veraltet kennzeichnen. Vor Freigabe einer externen PDF-Fassung soll eine persönliche Statusprüfung höchstens 48 Stunden zurückliegen. Genaue Fristen sind zu bestätigen. Frisches Abrufdatum macht eine historisch alte oder undatierte Aussage nicht automatisch aktuell.

**BE-005 – Statuswechsel:** Sobald ein Spieler einen Verein oder Berater hat, wird er aus der Trefferansicht entfernt und als „nicht mehr passend“ geführt. Die zulässige Historie bleibt nachvollziehbar. Ein Importfehler darf niemals als Vereinslosigkeit oder Beraterlosigkeit gewertet werden.

### 8.3 Quellen und Freigabe vor automatischem Abruf

**Prüfstand 10.09.2026:** FotMob untersagt nach seinen Nutzungsbedingungen unter anderem Scraping und kommerzielle Datennutzung ohne ausdrückliche schriftliche Zustimmung; systematische, regelmäßige und automatisierte Abrufe werden ebenfalls ausdrücklich untersagt. Der Footer enthält einen entsprechenden Hinweis. Die Transfermarkt-Nutzungsbedingungen ließen sich bei dieser Prüfung wegen einer Zugriffssperre nicht lesen. Für Transfermarkt wird daher weder ein Verbot im konkreten Umfang noch eine Erlaubnis behauptet. Eine passende Nutzungserlaubnis ist bislang für keine der beiden Quellen dokumentiert.

Quellen: [FotMob Terms of Use, Abschnitt Data Usage & Scraping](https://www.fotmob.com/tos.txt), [FotMob-Footer](https://www.fotmob.com/), [Transfermarkt-Nutzungsbedingungen – Abruf gesperrt](https://www.transfermarkt.de/intern/anb). Dies ist eine dokumentierte technische/projektbezogene Vorprüfung, keine rechtliche Freigabe.

| Gewünschte Quelle | Vorgesehene fachliche Rolle – noch zu verifizieren | Startvoraussetzung |
| --- | --- | --- |
| Transfermarkt | Kandidatensuche, Vereins-/Vertragssituation, ausdrückliche Beraterangaben, Vereins- und Marktwerthistorie | Nutzungsbedingungen, Feldabdeckung sowie Rechte für Abruf, Speicherung und Exposé-Ausgabe klären |
| FotMob | Ergänzende Identitäts-, Laufbahn- und Leistungsinformationen im tatsächlich verfügbaren Umfang | Ausdrückliche schriftliche Zustimmung bzw. geeignete Lizenz und erlaubter Zugangsweg |
| Freigegebener Datenfeed / eigene Erhebung | Ersatz oder Ergänzung, wenn gewünschte Quellen nicht nutzbar sind | Herkunft und Rechte ebenfalls dokumentieren; Anbieter und Kosten vor Beauftragung abstimmen |

**BE-006 – Quellenfreigabe:** Pro Quelle müssen erlaubte Felder, Suchumfang, Zugangsweg, Abrufhäufigkeit, Speicherdauer, Attribution, interne Nutzung und externe PDF-Weitergabe dokumentiert und freigegeben sein. Bild-, Vereinslogo- und Statistikrechte separat prüfen. Ein Drittanbieter-API-Angebot ist kein automatischer Nachweis ausreichender Weiterverwendungsrechte.

**BE-007 – Keine Umgehung:** Ohne Freigabe bleiben Quelladapter deaktiviert. CAPTCHA-, Login-, Paywall- und Zugriffssperren werden nicht umgangen. Bei ausdrücklichen Zugriffssperren pausiert der Adapter. Öffentlich abrufbare Seiten, robots.txt oder ein erreichbarer interner Endpunkt ersetzen keine passende Erlaubnis.

**BE-008 – Entwicklungsfähigkeit:** Datenmodell, Übersicht und PDF-Prozess müssen mit deutlich gekennzeichneten synthetischen Testdaten und rechtmäßig bereitgestellten Importdateien funktionieren. Manuelle Eingabe oder Dateiimport dienen nicht dazu, untersagte Datenverwendung zu umgehen. Kein Live-Crawling, solange Rechte und Suchumfang offen sind.

### 8.4 Regelmäßige Übernahme und Quellenüberwachung

**BE-009 – Suchumfang:** Ein freigegebenes Suchprofil bestimmt Wettbewerbe/Länder, Fußballkategorie, Altersbereich und gegebenenfalls weitere Eingrenzungen. Zusätzliche Kriterien sind als Filter konfigurierbar, aber nicht stillschweigend aktiv. Gefundene Treffer beziehen sich immer auf diese Abdeckung; keine unbelegte Vollständigkeitsbehauptung „alle verfügbaren Spieler weltweit“.

**Vorschlag für den Pilot:** zunächst Deutschland/DACH und Türkei; Start nur mit Erwachsenen. Diese Einschränkungen sind Vorschläge und keine bereits erteilte Freigabe. Die Länder der letzten Vereine, Nationalitäten und gewünschte Zielmärkte sind getrennte Filter.

**BE-010 – Zeitplan:** Nach Quellenfreigabe konfigurierbare regelmäßige Läufe mit Zeitzone Europe/Berlin. Vorschlag: täglich um 05:00 Uhr Änderungsprüfung, wöchentlich vollständiger Abgleich innerhalb des freigegebenen Suchprofils. Tatsächliche Intervalle und Umfang richten sich nach der erlaubten Nutzung. Noch kein Zeitplan wird durch dieses Dokument aktiviert.

**BE-011 – Robuster Import:**

- Jeder Lauf hat einen Status, Start-/Endzeit, Quelle, Suchprofil, Anzahl geprüfter, neuer, geänderter, unveränderter und fehlerhafter Datensätze.
- Seitennavigation und Teilabbrüche werden verfolgt; ein Lauf darf nur dann als vollständig gelten, wenn alle vorgesehenen Seiten/Segmente erfolgreich verarbeitet wurden.
- Gleiche Quelldatensätze dürfen bei Wiederholung keine doppelten Spieler oder Historienpunkte erzeugen.
- Erlaubte Lastgrenzen, begrenzte Wiederholungen und Wartezeiten bei temporären Fehlern einhalten. Bei 401/403, CAPTCHA oder Rechts-/Zugriffsproblemen pausieren statt alternative Zugriffsmethoden zu versuchen; bei 429 das vorgegebene Warteintervall berücksichtigen.
- Fehlerhafte Formate in eine Prüfliste stellen. Ein Parserfehler darf keine massenhaften Statusänderungen oder Löschungen auslösen.
- Teilerfolge bleiben sichtbar; erfolgreiche alte Daten werden nicht durch leere Antworten ersetzt. Fehlerhafte Daten dürfen nicht als frisch oder vollständig erscheinen.
- Neues/Geändertes innerhalb von 60 Minuten nach einem erfolgreichen freigegebenen Abruf in der Übersicht verfügbar machen (Vorschlag für den Pilot).

**BE-012 – Identitätsabgleich:** Pro Quelle stabile Spieler-ID und kanonische Profil-URL führen. Gleiche Namen reichen zum Zusammenführen nicht aus. Geburtsdatum, Nationalität und Stationen dienen als zusätzliche Hinweise. Namen mit Akzenten und unterschiedliche Schreibweisen berücksichtigen. Unsichere Zuordnungen werden manuell geprüft; Zusammenführungen müssen nachvollziehbar und korrigierbar sein.

### 8.5 Fachliches Datenmodell

Die folgenden Datenobjekte beschreiben fachliche Anforderungen, keine verbindliche Datenbank-/Frameworkentscheidung.

| Objekt | Mindestinhalt |
| --- | --- |
| Spieler | Interne ID, Name, Geburtsdatum soweit vorhanden, Nationalität(en), Haupt-/Nebenpositionen, Fuß, Größe, Aktivitätsstatus |
| Quellenzuordnung | Quelle, externe Spieler-ID, Profil-URL, Zuordnungsstatus, bestätigende Person |
| Statusbeleg | Verein bzw. Berater, normalisierter Status, Originalaussage im zulässigen Umfang, fachlicher Datenstand, Abrufzeit, Prüfstatus, Prüfer |
| Vereinsstation | Verein, Land, Wettbewerb, Beginn/Ende und Datumsgenauigkeit, Leih-/Transferart soweit belegt, Quelle |
| Marktwertpunkt | Originalbetrag, Währung, Bewertungsdatum, Anbieter, Abrufdatum, Quelle; unbekannt getrennt von null |
| Leistungsperiode | Saison, Verein, Wettbewerb, Einsätze, Minuten und positionsgeeignete Kennzahlen, Einheiten, Abdeckungsumfang, Quelle |
| Interne Einordnung | Stärken, offene Fragen und Einschätzungen mit Verfasser/Datum; klar von Fakten getrennt |
| Freigabe | Gegenstand, Prüfperson, Zeitpunkt, Ergebnis, zugrunde liegende Datenversion, erlaubter Verwendungszweck |
| PDF-Version | Spieler, Datenversion, Vorlagen-/CI-Version, Sprache, Zweck intern/extern, Status, Erstellungsdatum, Speicherreferenz, Freigabe |
| Importlauf | Quelle, Zeitraum, Suchprofil, Ergebniszähler, Fehler, Wiederanlaufpunkt, Vollständigkeit |
| Rechtefreigabe | Quelle/Inhalt, erlaubte Verarbeitung und Weitergabe, Umfang, Laufzeit, Nachweis, verantwortliche Person |

**BE-013 – Historien statt Überschreiben:** Vereinsstationen, Marktwertpunkte und relevante Statusänderungen werden mit ihrem jeweiligen Stand geführt. Korrekturen werden nachvollziehbar vorgenommen. Bereits vorhandene historische Quellwerte können nur bei erlaubtem Zugang übernommen werden; andernfalls beginnt die selbst beobachtete Historie beim ersten zulässigen Abruf. Historische Lücken dürfen nicht erfunden werden.

**BE-014 – Marktwertdarstellung:** Anbieter-Schätzung ausdrücklich als solche kennzeichnen, mit Datum und Währung. Nicht als Ablöse, Gehaltsforderung oder zugesicherten Verkaufspreis darstellen. Der „letzte verfügbare Marktwert“ darf bei alten Daten nicht als aktueller Wert ausgegeben werden. Fehlender Wert ist nicht 0 Euro. Verschiedene Anbieterwerte getrennt führen, nicht unbemerkt zu einer Kurve vermischen. Eine Zeitreihe benötigt mindestens zwei tatsächlich belegte Punkte; bei nur einem Wert Datum und Einzelwert zeigen.

**BE-015 – Bewertungsgrenzen:** Keine automatische Rangliste nach Marktwert als Ersatz für sportliche Prüfung. Zu Saisonstatistiken stets Wettbewerb und Zeitraum anzeigen; Karriere- und Saisonwerte nicht vermischen. Fehlende FotMob-Abdeckung blockiert ein ansonsten geprüftes Profil nicht, wird aber offen ausgewiesen.

### 8.6 Spielerübersicht und Detailansicht

**BE-016 – Übersicht:** Die Startansicht ist die Arbeitsliste, keine öffentliche Marketingseite. Sie enthält:

- Kennzahlen: passende Spieler, neu seit letzter Prüfung, ungeklärte Profile, veraltete Daten und fehlgeschlagene PDF-Aufträge. Kennzahlen immer auf den sichtbaren Suchumfang beziehen.
- Spalten: Name, Alter, Position, Nationalität, letzter Verein/Liga, vereinslos seit, Vereinsstatus, Beraterstatus, letzter belegter Marktwert mit Datum, Prüfdatum, Datenqualität, PDF-Status.
- Suche nach Name; Filter nach Status, Position, Land/Liga, Alter, Marktwertbereich, Zeit ohne Verein und Prüf-/PDF-Status. Fehlende Werte separat filterbar.
- Sortierung beispielsweise nach zuletzt aktualisiert, Name, Alter oder Marktwert; serverseitige Seitennavigation für größere Bestände.
- Getrennte Ansichten „Passende Spieler“, „Zu prüfen“ und „Nicht mehr passend“.
- Aktionen: Profil öffnen, Status prüfen, interne Notiz erfassen, PDF-Entwurf öffnen, PDF-Fassung freigeben. Kein Versandbutton im MVP.

**BE-017 – Spielerprofil:** Zusammenfassung mit beiden Eignungsnachweisen, Vereinslaufbahn als zeitliche Übersicht/Tabelle, Marktwertverlauf, belegten Saisonleistungen, Quellen und offenen Fragen. Vertragsstatus, Beraterstatus und eigene Beziehung zum Spieler bleiben getrennt. Zuordnung eines Profils zu Eleven Global bedeutet kein Mandat.

**BE-018 – Quellenkonflikte:** Widersprüchliche Angaben sichtbar nebeneinander zeigen. Keine stille Mehrheitsentscheidung. Eine menschliche Klärung verlangt Begründung und erhält einen nachvollziehbaren Stand. Ungeklärte kritische Statusangaben sperren die externe PDF-Freigabe.

### 8.7 PDF-Exposé in der Eleven-Global-CI

**BE-019 – Automatische Entwürfe:** Für jeden eindeutig zugeordneten, erstmals als passend aufgenommenen Spieler wird automatisch ein internes PDF erzeugt. Bei wesentlichen Datenänderungen entsteht eine neue Entwurfsfassung. Fehlende Marktwerte, Bilder oder Leistungsstatistiken dürfen die Erzeugung nicht verhindern; sie werden eindeutig kenntlich gemacht beziehungsweise ausgelassen. Die PDF-Erzeugung arbeitet als nachvollziehbarer Auftrag mit Status „ausstehend / erstellt / fehlgeschlagen“ und Wiederholungsmöglichkeit.

**BE-020 – Trennung von intern und extern:**

- Internes PDF: Wasserzeichen „ENTWURF – NUR INTERN“, Prüflücken sichtbar; kein automatischer Versand.
- Externe Vereinsfassung: ausschließlich aus einer persönlich freigegebenen Datenversion; interne Notizen, Kontaktrecherchen, ungesicherte Behauptungen und nicht lizenzierte Inhalte werden ausgeschlossen.
- Download der Vereinsfassung erst nach Freigabe und Prüfung der Weitergaberechte. Ein interner Entwurfsdownload bleibt innerhalb des geschützten Backends möglich.
- Keine Formulierung „unser Spieler“, „exklusiv vertreten“ oder Ähnliches ohne dokumentierte Grundlage. Für die externe Vorstellung sind erforderliche Berechtigungen und die Beziehung zum Spieler zu klären.
- Wesentliche Status-/Datenänderungen setzen die aktuelle externe Freigabe zurück. Frühere Fassungen werden als historisch/überholt erkennbar; sie dürfen nicht als aktuelle Fassung angeboten werden. Bereits extern verschickte Dateien können technisch nicht zuverlässig zurückgerufen werden.

**Vorgeschlagene Grundstruktur: zwei A4-Seiten, Deutsch.** Umfangreiche Stationen/Quellen dürfen auf einen klar gekennzeichneten Anhang ausweichen; Vollständigkeit hat Vorrang vor abgeschnittenem Inhalt. Englisch/Türkisch nach Bedarf, ausschließlich aus denselben geprüften Fakten.

| Bereich | Inhalt und Zweck |
| --- | --- |
| Seite 1: Spieler auf einen Blick | Name, Position, Alter, Nationalität, Fuß/Größe soweit belegt, Status mit Prüfdatum, letzter Verein, letzter verfügbarer Marktwert mit Bewertungsdatum |
| Seite 1: Kurzprofil | Knappes, persönlich geprüftes sportliches Profil; belegte Eckdaten getrennt von Einschätzungen; keine erfundene Verkaufsargumentation |
| Seite 1: Einordnung | Relevante letzte Saisonleistungen mit Wettbewerb/Minuten und klarer Datenabdeckung; bei fehlenden Daten entsprechender Hinweis |
| Seite 2: Laufbahn | Bisherige Vereine mit Zeitraum, Land/Liga und Leihkennzeichnung; Datumsunsicherheit sichtbar |
| Seite 2: Marktwert-Historie | Datierte Werte eines bezeichneten Anbieters; keine interpolierten oder erfundenen Werte; Quellen und Währung |
| Seite 2: Nachweise und Kontakt | Quellenlinks, Daten-/Prüfstand, Dokumentversion, gegebenenfalls belegte Video-Links und Eleven-Global-Kontakt |

**BE-021 – CI-Vorgaben:** Orientierung am aktuellen Website-Mockup: sehr dunkles Grün/Schwarz, Gold, zurückhaltende Typografie und großzügige Abstände. Die folgenden Werte sind aus der vorhandenen Gestaltung abgeleitete Arbeitswerte, noch kein verbindliches Markenhandbuch:

| CI-Element | Arbeitsvorgabe |
| --- | --- |
| Primärfarbe dunkel | `#070E0D` |
| Sekundäre Fläche | `#0E1716` |
| Goldakzent | `#C8A567` |
| Helle Schrift/Fläche | `#F0F1E9` |
| Kontakt | contact@eleven-global.com · +49 178 639 4229 |
| Absender | Eleven Global, eine Marke der STARKS Betriebs GmbH |

**Vorschlag Drucklayout:** überwiegend heller Seitenkörper mit dunklem Kopf/Fuß und Goldlinien, statt vollflächig schwarzer Seiten. Bildschirmwirkung, Kontrast und druckfreundliche Darstellung gemeinsam abnehmen. Logo-Datei, Hausschrift und Bildrechte müssen vor der endgültigen CI-Abnahme bereitgestellt oder bestätigt werden; keine vermeintlich offiziellen Markenassets neu erfinden. Freigegebene spätere CI-Änderungen werden über Vorlagenversionen nachvollzogen.

**BE-022 – PDF-Qualität und Versionierung:** Text muss durchsuchbar sein, verwendete Schriftzeichen korrekt darstellen und Quellenlinks anklickbar enthalten. Wiederholte Kopf-/Fußzeilen, Seitennummern, konsistente Zahlen-/Datumsformate; keine Überlappungen oder abgeschnittenen Tabellen. Kein Foto ohne Nutzungsrecht, kein Plattform-Screenshot als Ersatz. Dateiname beispielsweise `ElevenGlobal_Spieler-ID_DE_v03_2026-09-10.pdf`. Gleiche Daten-, Sprach- und Vorlagenversion erzeugen nicht mehrfach identische Fassungen. Vorschlag: ein Einzel-PDF innerhalb von 30 Sekunden, Sammelerzeugung im Hintergrund; Messung im vereinbarten Testumfang.

### 8.8 Zugang, Datenschutz und Betrieb

**BE-023 – Geschützter Bereich:** Backend und PDFs sind nicht öffentlich. Anmeldung und Berechtigung werden serverseitig für Listen, Datenabruf und Dokumentdownload geprüft. Keine öffentlich erratbaren Dokument-URLs. Eine ausgeblendete Navigation oder das Website-Passwort allein ersetzt keine Prüfung aller Backend-Endpunkte.

**Vorgeschlagene Rollen:** Administrator (Quellen/Betrieb/Nutzer), Recherche (Datenprüfung und interne Entwürfe), Freigabe (extern nutzbare Fassung). Für den Pilot kann Sevket Baykurd diese Rollen in einem Konto bündeln. Keine zusätzlichen Nutzer einladen, bevor sie benannt und berechtigt wurden.

**BE-024 – Nachvollziehbarkeit:** Import, manuelle Änderungen, Zusammenführungen, Prüfung, Freigabe und Export mit Nutzer, Zeitpunkt und Objektversion protokollieren. Keine Zugangsdaten oder vollständigen privaten Kontakt-/Formulardaten in Logs. Geheimnisse nur in dafür vorgesehenen Konfigurationen, niemals in GitHub oder im PDF.

**BE-025 – Datenminimierung und Rechte:** Vor Livebetrieb Zweck, Rechtsgrundlage, Informationspflichten, Speicherdauer, Korrektur-/Löschprozess und erforderliche Auftragsverarbeitung fachlich/rechtlich klären. Öffentlich sichtbare Spielerprofile sind nicht automatisch uneingeschränkt weiterverwendbar. Gesundheits-/Verletzungsdaten und private Telefonnummern sind im MVP nicht zu erheben. Umgang mit Minderjährigen benötigt eine gesonderte Entscheidung und Schutzprüfung.

**BE-026 – Speicherung und Löschung:** Produktive Daten dauerhaft serverseitig speichern, nicht nur im Browser. Lösch- und Aufbewahrungsfristen pro Datenart festlegen; Historien und PDF-Versionen sind nicht unbegrenzt aufzubewahren. Entfernung aus Quellen unterscheidet sich von Karriere-/Vereinsstatus und löst eine Prüfung aus. Anfragen auf Korrektur, Löschung oder Einschränkung müssen auch Dokumente, Suchindizes und den geregelten Backup-Zyklus berücksichtigen. Protokolle nur im erforderlichen und zulässigen Umfang erhalten.

**BE-027 – Betriebsfähigkeit:** Sichtbare Quellen-/Jobzustände, Fehlerzähler, letztes erfolgreiches Update, Sicherung und Wiederherstellung. Vorschlag für den Pilot: tägliche Sicherung, maximal 24 Stunden Datenverlust und Wiederherstellung innerhalb eines Arbeitstags; vor Produktivstart durch einen Wiederherstellungstest belegen. Für einen vereinbarten Testbestand von 5.000 synthetischen Profilen soll die erste Übersichtsseite unter üblichen Testbedingungen in höchstens zwei Sekunden antworten. Testumgebung und Messmethode bei Umsetzung dokumentieren.

### 8.9 Abnahmefälle

| ID | Prüffall | Erwartetes Ergebnis |
| --- | --- | --- |
| AT-01 | Vereinslos und ausdrücklich ohne Berater, aktuelle Nachweise | Genau ein Treffer in „Passende Spieler“; interner PDF-Auftrag entsteht |
| AT-02 | Vereinslos, Beraterfeld leer | Prüfliste statt positiver Treffer; keine externe Freigabe |
| AT-03 | Verein vorhanden oder Berater vorhanden | Kein Treffer der UND-Auswahl |
| AT-04 | Veralteter, widersprüchlicher oder undatierter kritischer Nachweis | Unsicherheit sichtbar; Prüfung statt ungeprüfter Freigabe |
| AT-05 | Gleicher Spieler aus beiden Quellen, sichere Identität | Ein kanonisches Profil mit zwei Quellenzuordnungen |
| AT-06 | Zwei gleichnamige Spieler, unklare Zuordnung | Keine automatische Zusammenführung |
| AT-07 | Identischer Import wird wiederholt | Keine zusätzlichen Profile oder doppelten Historienpunkte |
| AT-08 | 403, CAPTCHA, Parserfehler oder Teilabbruch | Adapter/Lauf entsprechend markiert, keine Umgehung und keine falschen Statusänderungen |
| AT-09 | Neuer Vereins- oder Beraterstatus | Aus Trefferliste entfernt; aktuelle externe Freigabe aufgehoben; frühere Fassung als historisch markiert |
| AT-10 | Fehlender Marktwert oder Foto | PDF wird ohne erfundene Werte/Bilder erstellt; Lücken sind erkennbar |
| AT-11 | Marktwert 0, alter Wert und fehlender Wert | Drei fachlich unterscheidbare Darstellungen; Anbieter und Datum sichtbar |
| AT-12 | Viele Stationen, lange Namen, türkische Zeichen | Lesbare PDF-Seiten/Anhänge ohne abgeschnittene Inhalte; Text und Links nutzbar |
| AT-13 | Person ohne Anmeldung oder ohne Freigaberolle | Keine unberechtigten Daten-/PDF-Zugriffe oder externe Freigaben |
| AT-14 | PDF aus freigegebener Datenversion | Alle Werte entsprechen exakt dieser Version; keine internen Notizen in Vereinsfassung |
| AT-15 | Wesentliche Änderung nach PDF-Freigabe | Neuer interner Entwurf, erneute persönliche Freigabe erforderlich |
| AT-16 | Fehlende/abgelaufene Quellen- oder Weitergaberechte | Kein Live-Abruf beziehungsweise keine externe Nutzung der betroffenen Inhalte |
| AT-17 | Sicherung wird wiederhergestellt | Spieler, Historien, Dokumente und Zugriffsrechte innerhalb des vereinbarten Rahmens wiederherstellbar |
| AT-18 | Fehlgeschlagener PDF-Auftrag | Fehler sichtbar und erneut ausführbar; keine unvollständige Fassung als erfolgreich markiert |

### 8.10 Umsetzungsreihenfolge für Codex

1. **M0 – Entscheidungen und Quellen:** GitHub-Ziel, Suchprofil, Rechte, CI und PDF-Umfang bestätigen. Ergebnis: abgestimmtes Lastenheft und klar aktivierbare Quellen.
2. **M1 – Datenmodell und Importbasis:** kanonische Spieler, Quellenzuordnungen, getrennte Statusbelege, Historien und synthetischer Import mit Validierung. UND-Logik und Fehlerfälle prüfen.
3. **M2 – Geschütztes Backend:** Übersicht, Detailprofil, Filter, Prüfliste, manuelle Klärung und Rollen. Keine Live-Quelle erforderlich.
4. **M3 – CI-Exposé:** versionierte interne PDFs, Vorschau, persönliche Freigabe, geschützter Download der Vereinsfassung und Änderungsinvalidierung. Fehlende Daten ausdrücklich testen.
5. **M4 – Genehmigte Datenquellen:** Adapter je Quelle separat aktivieren; Discovery und Aktualisierung im freigegebenen Umfang, Jobüberwachung und Sicherheitsgrenzen.
6. **M5 – Abnahme/Betrieb:** Testfälle, PDF-Sichtprüfung, Rechtekontrolle, Backup-/Restore-Test und kontrollierter Pilot. Nachrichtenversand bleibt außerhalb dieser Freigabe.

GitHub dient nach Wahl des konkreten Repositorys als gemeinsamer Arbeitsstand. Die GitHub-Erweiterung ist bei der Prüfung installiert; in diesem Arbeitsschritt wurde weder ein Ziel-Repository identifiziert noch ein Commit/Issue/PR dort erstellt. Website-Änderungen und Backend-Entwicklung erfolgen in getrennten Aufgaben/Branches. Produktive Spielerdaten, PDFs und Zugangsdaten gehören nicht ins Quellcode-Repository. Der bestehende Sites-Quellstand ist nicht automatisch mit GitHub synchronisiert.

### 8.11 Noch zu entscheidende Punkte

1. Welches GitHub-Repository ist verbindlich? Bitte URL oder `Eigentümer/Repository` angeben.
2. Welche Länder/Ligen und Fußballkategorie zuerst? Welche Altersgrenzen gelten? Vorschlag: Deutschland/DACH und Türkei, zunächst Erwachsene; nicht als bereits beschlossen behandeln.
3. Bestehen bereits schriftliche Nutzungsfreigaben oder Datenverträge für Transfermarkt/FotMob, einschließlich interner Speicherung und Weitergabe in Vereins-PDFs? Falls nicht, Beschaffungsweg und etwaiges Lizenzbudget festlegen.
4. Soll das allgemeine Exposé mit zwei A4-Seiten plus bedarfsweisem Quellen-/Laufbahnanhang starten? Vorschlag: Deutsch zuerst, später Englisch/Türkisch.
5. Liegen Original-Logo und Hausschrift vor? Soll die druckfreundliche helle Variante mit Schwarz-Gold-Akzenten gelten?
6. Bestätigung der Vorschläge zu Aktualität, Zeitplan, Pilotgröße und Betrieb sowie Benennung späterer weiterer Nutzer.

Diese offenen Punkte verhindern nicht die fachliche Abstimmung oder Entwicklung mit synthetischen Daten. Sie verhindern jedoch einen ungeprüften Live-Crawler, einen ungeklärten GitHub-Schreibzugriff beziehungsweise nicht freigegebene externe Spielerunterlagen.

## 9. Änderungsnachweis

- **08.09.2026:** ursprünglicher Arbeitsstand; Websitepriorität, Backend/Ansprache und späteres PDF vorgemerkt.
- **10.09.2026:** parallele Website-/Backend-Arbeit aufgenommen; UND-Kriterium konkretisiert; Übersicht, Quellenfreigabe, Statusqualität, Laufbahn/Marktwert-Historie, CI-Exposé, persönliche Freigabe, Abnahmetests und Codex-Arbeitspakete ergänzt. Kein Backend, Crawler oder PDF-Generator dadurch als umgesetzt erklärt.
