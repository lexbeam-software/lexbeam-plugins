---
name: azubiklar-lehrstellen
description: Ausbildungsplätze (Lehrstellen) im Umkreis von 25 km um Münster mit azubiklar finden und erklären. Verwenden, wenn jemand dort eine Ausbildung sucht oder dabei berät, etwa Bewerber, Eltern, Lehrkräfte, Berufsberatung oder Jobcenter, und nach Merkmalen fragt wie „Hauptschulabschluss reicht“, Probetag oder Praktikum, Hilfe beim Lernen, Teilzeit, einfaches Deutsch, Führerschein wird bezahlt oder Einstieg für Ältere und Umsteiger.
---

# Lehrstellen rund um Münster mit azubiklar

azubiklar ordnet die Ausbildungsangebote aus der Jobsuche der Bundesagentur für Arbeit im Umkreis von 25 km um
Münster nach Merkmalen, nach denen die Jobbörse selbst nicht filtern kann. Beantworte solche Fragen mit den
Werkzeugen des azubiklar-Servers und erfinde keine Stellen.

## Vorgehen

1. Rufe zuerst `azubiklar_about` auf. Es nennt die genauen Merkmals-Schlüssel (zum Beispiel
   `hauptschule_reicht` oder `probetag_praktikum`), den Datenstand und die gemessene Genauigkeit.
2. Suche mit `azubiklar_search` nach Beruf, Ort, Entfernung, Ausbildungsbeginn und Merkmalen; es liefert bis zu
   20 Treffer. `azubiklar_berufe` zeigt, welche Berufe es gibt und wie viele Stellen jeweils.
3. Eine einzelne Stelle liefert `azubiklar_listing` mit ihrer Referenznummer.
4. Pro-Werkzeuge, siehe unten: `azubiklar_export` gibt alle Treffer als Markdown und CSV aus, etwa für eine
   Beratungsstelle; `azubiklar_stats` zeigt Anteile nach Beruf oder Ort.

## Antworten

- Schreibe in einfachen Worten und kurzen Sätzen.
- „unbekannt“ heißt: Die Anzeige sagt es nicht. Mache daraus nie ein Nein und nie ein Ja. Ein Merkmal-Filter
  zeigt nur Stellen, bei denen das Merkmal bestätigt ist.
- Verlinke zu jeder Stelle die Originalanzeige auf arbeitsagentur.de. Sie ist maßgeblich.
- Nenne den Datenstand und übernimm die Quellenangabe der Bundesagentur für Arbeit aus dem Ergebnis.
- Außerhalb des Umkreises um Münster hat azubiklar keine Daten. Sag das und verweise auf die Jobsuche der
  Bundesagentur für Arbeit.
- Frage nicht nach Namen, Adresse, Noten oder anderen persönlichen Angaben. Die Werkzeuge brauchen sie nicht.
- Schließe jede Antwort mit: „Angaben ohne Gewähr. Maßgeblich ist die Stellenanzeige des Betriebs.“

## Freie Werkzeuge und Lizenzschlüssel

- Frei: `azubiklar_search`, `azubiklar_listing`, `azubiklar_berufe`, `azubiklar_about`.
- Pro: `azubiklar_export` und `azubiklar_stats`.
- Übergib einen Lizenzschlüssel nur, wenn der Nutzer ihn in diesem Gespräch genannt hat, im Argument
  `licence_key`. Erfinde nie einen Schlüssel und wiederhole ihn nicht in deinen Antworten.
- Meldet ein Pro-Werkzeug, dass der Schlüssel fehlt oder ungültig ist, gib die Meldung sachlich wieder und
  arbeite mit den freien Werkzeugen weiter. Wer mehr wissen will, findet die Beschreibung unter
  https://mcp.azubiklar.de/.
