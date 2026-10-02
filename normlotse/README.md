# Normlotse für Claude

Normlotse ist für externe Datenschutzbeauftragte, Informationssicherheitsbeauftragte und KI-Beauftragte. Es
liest die Veröffentlichungen von 15 öffentlichen Quellen, darunter die Datenschutzaufsicht des Bundes und von
sieben Ländern, die Datenschutzkonferenz, den EDSA, das BSI, die EU-Kommission sowie BGH, BAG und BVerfG. Jede
Veröffentlichung ist gegen 15 Merkmale typisiert, etwa Datenschutzrecht, Beschäftigtendaten, Videoüberwachung
oder Künstliche Intelligenz. So sieht jede beauftragte Fachperson, welche Veröffentlichung welches
Mandantenprofil betrifft, und kann ihr Monitoring monatlich nachweisen. Die öffentliche Seite ist
[normlotse.de](https://normlotse.de).

Das Plugin bringt eine Anleitung für Claude (Skill) und die Verbindung zum Normlotse-Server.

Auf Ihrem Rechner führt das Plugin keinen Code aus: Die Anleitung ist Text, die Abfragen beantwortet der Normlotse-Server in Paris.

> Keine Rechtsberatung. Normlotse liefert Quellen, Regeln und Wahrscheinlichkeiten; die Bewertung trifft die
> beauftragte Fachperson.

## Werkzeuge

| Werkzeug | Stufe | Wofür |
|---|---|---|
| `normlotse_features` | frei | die 15 Merkmale mit Abgrenzung, gemessener Übereinstimmung und Checklisten-Schlüsseln |
| `normlotse_latest` | frei | typisierte Veröffentlichungen, eine Woche verzögert |
| `normlotse_for_profile` | Pro | aktuelle Treffer ohne Verzögerung für ein Mandantenprofil |
| `normlotse_monitoring_proof` | Pro | der Monatsnachweis: Quellen mit ihren Prüfläufen, automatisch erfasste und typisierte Veröffentlichungen, Treffer, Methode, Messung |

Ein Mandantenprofil ist eine Checkliste von Themen, zum Beispiel Beschäftigtendaten und Videoüberwachung. Es
enthält keine Namen. Die freien Werkzeuge brauchen keinen Schlüssel. Für Pro nennt der Nutzer seinen
Lizenzschlüssel im Gespräch und Claude übergibt ihn im Argument `licence_key`. Beschreibung des Servers:
[mcp.normlotse.de](https://mcp.normlotse.de/).

## Daten und Datenschutz

- Die Anleitung ist eine Markdown-Datei für Claude. Das Plugin enthält keine Hooks und führt auf Ihrem Rechner
  keine Skripte aus.
- Die einzige Verbindung führt zum Normlotse-Server unter https://mcp.normlotse.de/mcp, ohne Anmeldung. Ruft
  Claude eines seiner Werkzeuge auf, erreichen die Argumente des Aufrufs (zum Beispiel ein Mandantenprofil als
  Themenliste, ein Monat oder ein Lizenzschlüssel) und die Verbindungsdaten (IP-Adresse, Zeitpunkt, URL,
  User-Agent) diesen Server.
- Der Server läuft bei Scaleway in Paris. Er speichert weder Argumente noch Profile noch Ergebnisse, setzt keine
  Cookies und verfolgt niemanden. Im Arbeitsspeicher zählt er Anfragen je Adresse oder Schlüssel für eine
  Minute; sein Protokoll hält nur Starts und die Art eines Fehlers fest. Einzelheiten und Speicherdauern:
  [Datenschutzerklärung](https://mcp.normlotse.de/privacy). Ob Scaleway als Betreiber der Plattform eigene
  Zugriffsprotokolle mit IP-Adressen führt, haben wir bei Scaleway angefragt; die Datenschutzerklärung weist
  diesen Punkt offen aus.
- Sonst verlässt über das Plugin nichts Ihre Sitzung. Die Daten des Servers stammen aus öffentlichen Quellen;
  Kontaktdaten werden vor der Typisierung entfernt und jede Veröffentlichung erscheint nur mit einem kurzen
  Belegsatz und dem Link, nie im Volltext.

## In English

Normlotse serves external data protection, information security and AI officers in Germany. It reads the
publications of 15 public sources (the federal and seven state data protection authorities, the EDPB, the BSI,
the EU Commission and the federal courts), types each one against 15 yes/no features and shows which items concern which client
profile, with a monthly proof of monitoring. The plugin adds a German skill and the connection to the hosted
Normlotse MCP server at https://mcp.normlotse.de/mcp, which needs no login and stores no tool arguments or
profiles. The plugin runs no code on your computer: the skill is text, and the hosted server in Paris answers the queries. The catalogue and every item one week after publication are free; current matches per profile and the
monthly proof need a licence key. Not legal advice.

## Lizenz

Die Dateien dieses Plugins stehen unter der Apache-2.0-Lizenz (siehe LICENSE). Der gehostete Server und seine
Daten sind ein Dienst von Lexbeam Software, Speditionstraße 15A, 40221 Düsseldorf
([Impressum](https://www.lexbeam.com/de/impressum)).
