---
name: installflow-netzbetreiber
description: Anforderungen der Stromnetzbetreiber in Nordrhein-Westfalen mit Installflow nachschlagen. Verwenden, wenn ein Elektroinstallateur, Planer oder Bauherr wissen will, welcher Verteilnetzbetreiber zuständig ist und was er für Wallbox, PV-Anlage, Wärmepumpe, Speicher oder Hausanschluss verlangt, etwa TAB NS, eigene Ergänzungen, Anmeldeportal, Formulare, Zählerplatz, Inbetriebsetzung oder § 14a EnWG.
---

# Netzbetreiber-Regeln mit Installflow

Installflow kennt die öffentlich veröffentlichten Anforderungen der 113 Verteilnetzbetreiber in
Nordrhein-Westfalen. Beantworte solche Fragen mit den Werkzeugen des Installflow-Servers, nicht aus dem
Gedächtnis: Die Regeln unterscheiden sich von Netzbetreiber zu Netzbetreiber und ändern sich.

## Vorgehen

1. Netzbetreiber bestimmen: `installflow_find_operator` mit Ort, Namen oder MaStR-Nummer. Liefert die Suche
   mehrere Kandidaten, nenne sie und frage nach Straße oder Ortsteil. Rate nie, welches Netz zuständig ist.
2. Regeln lesen: `installflow_operator_rules` mit der Kennung aus Schritt 1.
3. Für ein konkretes Vorhaben liefert `installflow_checklist` die Checkliste. Erlaubte Vorhaben: `wallbox`,
   `pv`, `waermepumpe`, `speicher`, `hausanschluss`. Das ist ein Pro-Werkzeug, siehe unten.
4. Fragt jemand, wie verlässlich die Angaben sind oder wie viele Netzbetreiber abgedeckt sind, rufe zuerst
   `installflow_coverage` auf und antworte mit dessen Zahlen.

## Antworten

- Nenne zu jeder Anforderung die Quelle als Link und den Stand oder das Prüfdatum aus dem Ergebnis.
- „nicht erkennbar“ bleibt „nicht erkennbar“. Mache daraus weder eine Zusage noch ein Nein. Verweise dann auf
  das Dokument oder die Netzanschluss-Stelle des Netzbetreibers.
- Punkte mit der Markierung `generic` stammen aus dem BDEW-Mustertext, nicht aus einem eigenen Dokument des
  Netzbetreibers. Sag das dazu.
- Außerhalb von Nordrhein-Westfalen hat Installflow keine Daten. Sag das offen, statt zu schätzen.
- Schließe jede Antwort mit: „Keine Rechtsberatung, keine Gewähr. Maßgeblich sind die Dokumente des
  Netzbetreibers.“

## Freie Werkzeuge und Lizenzschlüssel

- Frei: `installflow_find_operator`, `installflow_operator_rules`, `installflow_coverage`.
- Pro: `installflow_checklist` und `installflow_changes`. Datenlizenz: `installflow_compare`.
- Übergib einen Lizenzschlüssel nur, wenn der Nutzer ihn in diesem Gespräch genannt hat, im Argument
  `licence_key`. Erfinde nie einen Schlüssel und wiederhole ihn nicht in deinen Antworten.
- Meldet ein Pro-Werkzeug, dass der Schlüssel fehlt oder ungültig ist, gib die Meldung sachlich wieder und
  arbeite mit den freien Werkzeugen weiter. Wer mehr wissen will, findet die Beschreibung unter
  https://mcp.installflow.de/.
