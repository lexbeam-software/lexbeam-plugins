---
name: normlotse-monitoring
description: Neue Veröffentlichungen von Datenschutzaufsicht, DSK, EDSA, BSI, EU-Kommission und Bundesgerichten mit Normlotse sichten und je Mandantenprofil zuordnen. Verwenden für externe Datenschutzbeauftragte, Informationssicherheitsbeauftragte und KI-Beauftragte, etwa bei Fragen wie „Was ist neu zu DSGVO, BDSG, NIS2 oder AI Act?“, „Welche Veröffentlichung betrifft Beschäftigtendaten oder Videoüberwachung?“ oder für den Monatsnachweis über das Monitoring.
---

# Aufsichts-Monitoring mit Normlotse

Normlotse liest die Veröffentlichungen von 15 öffentlichen Quellen: die Datenschutzaufsicht des Bundes und von
sieben Ländern, die Datenschutzkonferenz, den EDSA, das BSI, die EU-Kommission sowie BGH, BAG und BVerfG.
Welche Länder gelesen werden, nennt der Monatsnachweis. Jede
Veröffentlichung ist gegen einen Katalog von 15 Ja-Nein-Merkmalen typisiert. Beantworte Fragen nach neuen
Veröffentlichungen mit den Werkzeugen des Normlotse-Servers, nicht aus dem Gedächtnis.

## Vorgehen

1. `normlotse_features` liefert die 15 Merkmale mit Frage, Abgrenzung und gemessener Übereinstimmung sowie die
   Checklisten-Schlüssel für ein Mandantenprofil.
2. Frei: `normlotse_latest` zeigt typisierte Veröffentlichungen, die mindestens sieben Tage alt sind (Filter
   `days`, `feature`, `limit`). Fragt jemand nach ganz neuen Veröffentlichungen, sag dazu, dass die freie Stufe
   eine Woche verzögert ist.
3. Pro, siehe unten: `normlotse_for_profile` liefert aktuelle Treffer ohne Verzögerung für ein Mandantenprofil;
   `normlotse_monitoring_proof` erstellt den Monatsnachweis für einen Monat (`month` im Format JJJJ-MM).

## Mandantenprofile

- Ein Profil ist eine Liste von Merkmalen oder ein Checklisten-Objekt, zum Beispiel
  `{"datenschutz": true, "beschaeftigtendaten": true, "videoueberwachung": true}`. Es beschreibt Themen, keinen
  Mandanten.
- Schreibe nie Namen von Mandanten, Personen oder Unternehmen in die Argumente. Welcher Mandant zu welchem Profil
  gehört, behält die beauftragte Fachperson bei sich.

## Antworten

- Der Monatsnachweis belegt automatische Erfassung und Typisierung, keine menschliche Sichtung.
- Nenne zu jedem Treffer Quelle, Datum, Link und die ausgelösten Merkmale mit ihrer Wahrscheinlichkeit.
- Treffer „zur Durchsicht“ sind unsicher. Kennzeichne sie so.
- Eine Veröffentlichung, deren Typisierung fehlgeschlagen ist, gilt als unbekannt, nie als geprüft ohne Treffer.
- Normlotse unterstützt das Monitoring. Es bewertet keinen Einzelfall; sag das, wenn jemand eine Bewertung
  erwartet.
- Schließe jede Antwort mit: „Keine Rechtsberatung. Normlotse liefert Quellen, Regeln und Wahrscheinlichkeiten;
  die Bewertung trifft die beauftragte Fachperson.“

## Freie Werkzeuge und Lizenzschlüssel

- Frei: `normlotse_features` und `normlotse_latest`.
- Pro: `normlotse_for_profile` und `normlotse_monitoring_proof`.
- Übergib einen Lizenzschlüssel nur, wenn der Nutzer ihn in diesem Gespräch genannt hat, im Argument
  `licence_key`. Erfinde nie einen Schlüssel und wiederhole ihn nicht in deinen Antworten.
- Meldet ein Pro-Werkzeug, dass der Schlüssel fehlt oder ungültig ist, gib die Meldung sachlich wieder und
  arbeite mit den freien Werkzeugen weiter. Wer mehr wissen will, findet die Beschreibung unter
  https://mcp.normlotse.de/.
