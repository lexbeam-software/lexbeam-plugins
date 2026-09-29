# azubiklar für Claude

azubiklar findet Ausbildungsplätze im Umkreis von 25 km um Münster und ordnet sie nach Merkmalen, nach denen die
Jobbörse der Bundesagentur für Arbeit selbst nicht filtern kann: Hauptschulabschluss reicht, Probetag oder
Praktikum, Hilfe beim Lernen, Hilfe beim Wohnen, offen für Menschen mit Behinderung, einfaches Deutsch reicht,
Teilzeit möglich, Führerschein wird bezahlt, auch für Ältere und Umsteiger, Geflüchtete willkommen sowie Abitur
oder Führerschein nötig. Jede Stelle verlinkt die Originalanzeige auf arbeitsagentur.de. Die öffentliche Seite
ist [azubiklar.de](https://azubiklar.de).

Das Plugin bringt eine Anleitung für Claude (Skill) und die Verbindung zum azubiklar-Server. Es hilft allen, die
rund um Münster eine Ausbildung suchen oder dabei beraten: Bewerbern, Eltern, Lehrkräften, der Berufsberatung und
Jobcentern.

> Angaben ohne Gewähr. Maßgeblich ist die Stellenanzeige des Betriebs.

## Werkzeuge

| Werkzeug | Stufe | Wofür |
|---|---|---|
| `azubiklar_search` | frei | Stellen nach Beruf, Ort, Entfernung, Beginn und Merkmalen, bis zu 20 Treffer |
| `azubiklar_listing` | frei | eine Stelle mit allen Merkmalen und dem Link zur Anzeige |
| `azubiklar_berufe` | frei | alle Berufe mit der Zahl ihrer Stellen |
| `azubiklar_about` | frei | Abdeckung, Datenstand, Merkmale in einfachen Worten und gemessene Genauigkeit |
| `azubiklar_export` | Pro | alle Treffer als Markdown und CSV, etwa für eine Beratungsstelle |
| `azubiklar_stats` | Pro | Anteile nach Beruf oder Ort, etwa wie oft der Hauptschulabschluss reicht |

Ein Merkmal, das die Anzeige nicht klar nennt, heißt „unbekannt“, nie „nein“. Die freien Werkzeuge brauchen
keinen Schlüssel. Für Pro nennt der Nutzer seinen Lizenzschlüssel im Gespräch und Claude übergibt ihn im Argument
`licence_key`. Beschreibung des Servers: [mcp.azubiklar.de](https://mcp.azubiklar.de/).

## Daten und Datenschutz

- Die Anleitung ist eine Markdown-Datei für Claude. Das Plugin enthält keine Hooks und führt auf Ihrem Rechner
  keine Skripte aus.
- Die einzige Verbindung führt zum azubiklar-Server unter https://mcp.azubiklar.de/mcp, ohne Anmeldung. Ruft
  Claude eines seiner Werkzeuge auf, erreichen die Argumente des Aufrufs (zum Beispiel ein Beruf, ein Ort oder
  ein Lizenzschlüssel) und die Verbindungsdaten (IP-Adresse, Zeitpunkt, URL, User-Agent) diesen Server.
- Der Server läuft bei Scaleway in Paris. Er speichert weder Argumente noch Ergebnisse, setzt keine Cookies und
  verfolgt niemanden. Im Arbeitsspeicher zählt er Anfragen je Adresse oder Schlüssel für eine Minute; sein
  Protokoll hält nur Starts und die Art eines Fehlers fest. Einzelheiten und Speicherdauern:
  [Datenschutzerklärung](https://mcp.azubiklar.de/privacy). Ob Scaleway als Betreiber der Plattform eigene
  Zugriffsprotokolle mit IP-Adressen führt, haben wir bei Scaleway angefragt; die Datenschutzerklärung weist
  diesen Punkt offen aus.
- Sonst verlässt über das Plugin nichts Ihre Sitzung. Die Werkzeuge brauchen keine persönlichen Angaben der
  Suchenden. Die Stellendaten enthalten keine Ansprechpartner, E-Mail-Adressen oder Telefonnummern.
- Quelle der Stellen: BUNDESAGENTUR FÜR ARBEIT (BA), Jobsuche, https://www.arbeitsagentur.de/jobsuche/. Jedes
  Ergebnis nennt Jahr und Stand.

## In English

azubiklar finds apprenticeship (Ausbildung) listings within 25 km of Münster, Germany, and types them for access
attributes the Federal Employment Agency's job portal cannot filter by, such as "a lower secondary school
certificate is enough", "trial day or internship" or "learning support". Every listing links to its original
posting on arbeitsagentur.de. The plugin adds a German skill and the connection to the hosted azubiklar MCP
server at https://mcp.azubiklar.de/mcp, which needs no login and stores no tool arguments. Four tools are free;
the export and the statistics need a licence key. Answers are in German.

## Lizenz

Die Dateien dieses Plugins stehen unter der Apache-2.0-Lizenz (siehe LICENSE). Der gehostete Server und seine
Daten sind ein Dienst von Lexbeam Software, Speditionstraße 15A, 40221 Düsseldorf
([Impressum](https://www.lexbeam.com/de/impressum)).
