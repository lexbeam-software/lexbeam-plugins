---
name: installflow-netzbetreiber
description: Anforderungen der Stromnetzbetreiber in Nordrhein-Westfalen mit Installflow nachschlagen. Verwenden, wenn ein Elektroinstallateur, Planer oder Bauherr wissen will, was ein Verteilnetzbetreiber für Wallbox, PV-Anlage, Wärmepumpe, Speicher oder Hausanschluss verlangt, etwa TAB NS, eigene Ergänzungen, Anmeldeportal, Formulare, Zählerplatz, Inbetriebsetzung oder § 14a EnWG, oder wenn er einen Netzbetreiber nach Namen, Sitz oder MaStR-Nummer sucht.
---

# Netzbetreiber-Regeln mit Installflow

Installflow erfasst alle 113 Verteilnetzbetreiber in Nordrhein-Westfalen und ihre veröffentlichten
Anforderungen; für die meisten liegen Regeln vor, `installflow_coverage` nennt den Stand. Beantworte solche
Fragen mit den Werkzeugen des Installflow-Servers, nicht aus dem Gedächtnis: Die Regeln unterscheiden sich von
Netzbetreiber zu Netzbetreiber und ändern sich.

## Vorgehen

1. Netzbetreiber bestimmen: `installflow_find_operator` sucht nach Namen, nach dem Sitz laut
   Marktstammdatenregister oder nach der MaStR-Nummer. Ein Treffer über den Ort heißt nur, dass der
   Netzbetreiber dort seinen Sitz hat; das Netz an einer bestimmten Adresse kann ein anderer betreiben. Welcher
   Netzbetreiber zuständig ist, steht auf der Stromrechnung oder in den Unterlagen zum Netzanschluss. Nennt der
   Nutzer nur einen Ort, frage danach und zeige die Treffer als Kandidaten, nicht als Antwort. Ohne Treffer sag
   das und frage nach dem Namen oder der MaStR-Nummer. Rate nie, welches Netz zuständig ist.
2. Regeln lesen: `installflow_operator_rules` mit der Kennung aus Schritt 1.
3. Für ein konkretes Vorhaben liefert `installflow_checklist` die Checkliste. Erlaubte Vorhaben: `wallbox`,
   `pv`, `waermepumpe`, `speicher`, `hausanschluss`. Das ist ein Pro-Werkzeug, siehe unten.
4. Fragt jemand, wie verlässlich die Angaben sind oder wie viele Netzbetreiber abgedeckt sind, rufe zuerst
   `installflow_coverage` auf und antworte mit dessen Zahlen.

## Antworten

- `not_required` heißt: Merkmal in den Dokumenten nicht erkannt, nur Mustertext gelesen oder keine eigenen Dokumente vorhanden. Das ist nie eine Befreiung; lies `interpretation` und `note`.
- Nenne zu jeder Anforderung die Quelle als Link und den Stand oder das Prüfdatum aus dem Ergebnis.
- „nicht erkennbar“ bleibt „nicht erkennbar“. Mache daraus weder eine Zusage noch ein Nein. Verweise dann auf
  das Dokument oder die Netzanschluss-Stelle des Netzbetreibers.
- Punkte mit der Markierung `generic` sind nicht in eigenen Dokumenten des Netzbetreibers belegt: Die Antwort
  stammt aus dem unveränderten BDEW-Mustertext oder es liegen keine eigenen Dokumente vor. Sag das dazu.
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
