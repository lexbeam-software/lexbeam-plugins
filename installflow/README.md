# Installflow für Claude

Installflow zeigt Elektroinstallateuren in Nordrhein-Westfalen, was ihr Netzbetreiber verlangt: die TAB NS mit
Stand, die eigenen Ergänzungen des Netzbetreibers über den BDEW-Mustertext hinaus, das Anmeldeportal und die
Formulare sowie die Seite zu § 14a EnWG. Jede Angabe trägt den Link zur Quelle und das Prüfdatum. Erfasst sind
alle 113 Verteilnetzbetreiber in NRW: Für 63 liegen die Regeln vollständig vor, für 39 teilweise, bei 11 fanden
sich keine Dokumente (Stand 25.09.2026; den aktuellen Stand nennt `installflow_coverage`). Die öffentliche Seite
ist [installflow.de](https://installflow.de).

Das Plugin bringt eine Anleitung für Claude (Skill) und die Verbindung zum Installflow-Server. Claude findet
damit einen Netzbetreiber nach Namen, Sitz oder MaStR-Nummer, liest seine Regeln und stellt mit einem
Pro-Schlüssel die Checkliste für ein Vorhaben zusammen: Wallbox, PV-Anlage, Wärmepumpe, Speicher oder
Hausanschluss. Welcher Netzbetreiber für eine Adresse zuständig ist, steht auf der Stromrechnung oder in den
Unterlagen zum Netzanschluss.

> Keine Rechtsberatung, keine Gewähr. Maßgeblich sind die Dokumente des Netzbetreibers.

## Werkzeuge

| Werkzeug | Stufe | Wofür |
|---|---|---|
| `installflow_find_operator` | frei | einen Netzbetreiber nach Namen, Sitz oder MaStR-Nummer finden |
| `installflow_operator_rules` | frei | die Regeln eines Netzbetreibers mit Quelle und Datum |
| `installflow_coverage` | frei | Abdeckung, Datenstand und gemessene Genauigkeit |
| `installflow_checklist` | Pro | die Checkliste für ein Vorhaben bei einem Netzbetreiber |
| `installflow_changes` | Pro | Änderungen zwischen zwei Datenständen seit einem Datum |
| `installflow_compare` | Datenlizenz | eine Vergleichstabelle über Netzbetreiber, als Markdown und CSV |

Die freien Werkzeuge brauchen keinen Schlüssel. Für Pro und die Datenlizenz nennt der Nutzer seinen
Lizenzschlüssel im Gespräch und Claude übergibt ihn im Argument `licence_key`. Beschreibung des Servers:
[mcp.installflow.de](https://mcp.installflow.de/).

## Daten und Datenschutz

- Die Anleitung ist eine Markdown-Datei für Claude. Das Plugin enthält keine Hooks und führt auf Ihrem Rechner
  keine Skripte aus.
- Die einzige Verbindung führt zum Installflow-Server unter https://mcp.installflow.de/mcp, ohne Anmeldung. Ruft
  Claude eines seiner Werkzeuge auf, erreichen die Argumente des Aufrufs (zum Beispiel ein Ortsname oder ein
  Lizenzschlüssel) und die Verbindungsdaten (IP-Adresse, Zeitpunkt, URL, User-Agent) diesen Server.
- Der Server läuft bei Scaleway in Paris. Er speichert weder Argumente noch Ergebnisse, setzt keine Cookies und
  verfolgt niemanden. Im Arbeitsspeicher zählt er Anfragen je Adresse oder Schlüssel für eine Minute; sein
  Protokoll hält nur Starts und die Art eines Fehlers fest. Einzelheiten und Speicherdauern:
  [Datenschutzerklärung](https://mcp.installflow.de/privacy). Ob Scaleway als Betreiber der Plattform eigene
  Zugriffsprotokolle mit IP-Adressen führt, haben wir bei Scaleway angefragt; die Datenschutzerklärung weist
  diesen Punkt offen aus.
- Sonst verlässt über das Plugin nichts Ihre Sitzung. Die Daten des Servers stammen aus öffentlichen Dokumenten
  der Netzbetreiber und enthalten nur geschäftliche Kontaktstellen, keine personenbezogenen Daten.

## In English

Installflow tells electricians in North Rhine-Westphalia what their electricity grid operator requires for a
wallbox, a PV system, a heat pump, battery storage or a house connection: the operator's technical connection
rules (TAB NS), its own supplements, its registration portal and forms, and its page on § 14a EnWG, each with a
source link and a date. It lists all 113 distribution grid operators in the state and has rules for 102 of them
(status 25.09.2026). The plugin adds a German
skill and the connection to the hosted Installflow MCP server at https://mcp.installflow.de/mcp, which needs no
login and stores no tool arguments. Three tools are free; the checklist and the change report need a licence
key. Answers are in German and are not legal advice.

## Lizenz

Die Dateien dieses Plugins stehen unter der Apache-2.0-Lizenz (siehe LICENSE). Der gehostete Server und seine
Daten sind ein Dienst von Lexbeam Software, Speditionstraße 15A, 40221 Düsseldorf
([Impressum](https://www.lexbeam.com/de/impressum)).
