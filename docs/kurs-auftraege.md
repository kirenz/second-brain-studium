# Kursaufträge: ein Agenten-Auftrag je Termin

Ab dem Werkzeugtermin arbeitet der Agent in der eigenen Ablage durchgehend mit. Von Termin 2 bis Termin 8 gibt es je einen kleinen Auftrag zum Thema des Termins. Jeder Auftrag enthält einen Teil, den die Person selbst leistet und begründet, denn die Klausur läuft ohne KI. Die Daten der Termine stehen im Kursplan; Neles Beispieldaten folgen einem fiktiven Kalender.

**Voraussetzungen**

- Die eigene Ablage ist als Projekt in Antigravity geöffnet (siehe [Erste Schritte](erste-schritte.md)).
- Das Permission Preset steht auf Default.
- Wer kein eigenes KI-Abo nutzt, arbeitet im Team an einem Gerät mit. Das [Delegationsprotokoll](delegationsprotokoll.md) führt jede Person in der eigenen Ablage.
- Platzhalter in `{…}` werden vor dem Abschicken durch eigene Angaben ersetzt.

**Ablauf je Auftrag:** wie im [Demo-Drehbuch](demo-drehbuch.md): neue Unterhaltung, Prompt abschicken, Ergebnis mit „Erwartet“ vergleichen, über **Review** den Diff lesen. Danach den Eintrag ins Delegationsprotokoll ergänzen (Prompt dort unter „Einen Eintrag ergänzen“).

> **Achtung:** In die Ablage kommen nur Vornamen und Rollen des eigenen Teams. Keine Nachnamen mit Bewertungen, keine Kontaktdaten, keine Gesundheitsangaben.

| Termin | Auftrag an den Agenten | Schreibt |
|---|---|---|
| Werkzeugtermin | Protokoll beginnen, Schätzung notieren, Zeiterfassung starten | Protokoll |
| 2 Prioritäten-Werkstatt | Zeiterfassung auswerten, Wochenplan entwerfen | nichts, dann eine neue Datei |
| 3 Kanalarchitektur | Entwurf auf Lücken prüfen | nichts |
| 4 Meeting-Makeover | Mitschrift der zweiten Runde ins Projektlog | einen Logeintrag |
| 5 Board-Werkstatt | Fertig-Kriterien gegenprüfen | nichts |
| 6 Sprint-Simulation | Durchsatz und Retro ins Projektlog | einen Logeintrag |
| 7 OKR-Werkstatt | OKR-Entwurf prüfen | nichts |
| 8 Feedback und Retro | Weg A ins Protokoll | eine Protokollzeile |
| 9 Delegationsmatrix | kein neuer Auftrag, Protokoll mitbringen | nichts |

## Werkzeugtermin: Protokoll beginnen und Zeiterfassung starten

**Voraussetzung:** Auftrag 3 im [Demo-Drehbuch](demo-drehbuch.md) ist erledigt, die erste Protokollzeile steht.

```text
Ersetze in docs/delegationsprotokoll.md unter „Schätzung vor der Zeiterfassung“ Neles Angaben durch meine: Datum {JJJJ-MM-TT}, Fokusarbeit {…} %, Abstimmung {…} %, Kleinkram {…} %. Setze bei „Gemessen“ und „Meine Deutung“ jeweils „offen“. Ändere keine andere Zeile und keine andere Datei.
```

**Erwartet:** Drei Zeilen mit den eigenen Werten, zusammen 100 %. „Gemessen“ und „Meine Deutung“ stehen auf „offen“.
**Schreibgrenze:** Eine Datei, nur der Abschnitt „Schätzung“. Die Tabelle „Einträge“ bleibt unverändert.
**Selbst:** Die Schätzung entsteht ohne Agent und vor dem ersten Eintrag. Eine nachträgliche Schätzung macht den Vergleich in Termin 2 wertlos.
**Ins Protokoll:** Die erste Zeile aus Auftrag 3 genügt für heute.

### Zeiterfassung für eine Woche

Die Zeiterfassung läuft eine Woche, vom Werkzeugtermin bis Termin 2. Sie ist ein Experiment, kein Dauerwerkzeug.

**Voraussetzungen**

- Die Schätzung steht im Protokoll.
- Ein Werkzeug ist gewählt: Clockify, eine andere App oder eine einfache Tabelle. Ein weiteres Konto ist nicht nötig.
- Die Kategorien sind klar. **Fokusarbeit:** konzentrierte Arbeit an einer Aufgabe. **Abstimmung:** Arbeit mit anderen, etwa Teamtreffen und Teamchat. **Kleinkram:** kurze Organisationsaufgaben allein, etwa Mails sichten oder Dateien sortieren.

**Schritte**

1. Legen Sie die drei Kategorien im gewählten Werkzeug an.
2. Erfassen Sie eine Woche lang jeden Arbeitsblock für Studium und Projekt.
3. Notieren Sie je Block Datum, Beginn, Ende, Tätigkeit und Kategorie.
4. Ordnen Sie jeden Block genau einer Kategorie zu.
5. Lassen Sie Vorlesungen, Seminar und Schichten weg. Diese Termine stehen in den Rhythmen.
6. Speichern Sie die Einträge vor Termin 2 als CSV-Datei.
7. Entfernen Sie Spalten mit Namen oder E-Mail-Adressen.
8. Legen Sie die Datei als `00_Inbox/zeiterfassung-{Startdatum}.csv` ab.
9. Prüfen Sie die Datei. Kriterium: Jede Zeile hat Datum, Beginn, Ende und eine der drei Kategorien.

Aufbau und Umfang zeigt Neles [Beispieldatei](../00_Inbox/zeiterfassung-beispielwoche.csv) mit 29 Zeilen.

> **Achtung:** Die Spalte „Tätigkeit“ liest der Agent mit. Dort nur Vornamen und keine Kontaktdaten eintragen.

## Termin 2: Zeiterfassung auswerten und Wochenplan entwerfen

**Voraussetzung:** Die eigene Exportdatei oder Tabelle liegt als CSV in `00_Inbox/`, an derselben Stelle wie Neles `zeiterfassung-beispielwoche.csv`. Die Schätzung steht im Protokoll.

```text
Werte 00_Inbox/{Dateiname}.csv aus. Summiere die Minuten je Tag und je Kategorie (Fokusarbeit, Abstimmung, Kleinkram) und nenne die Anteile an der Gesamtzeit in Prozent. Stelle die Anteile meiner Schätzung in docs/delegationsprotokoll.md gegenüber. Antworte mit zwei Tabellen im Chat und ändere keine Datei.
```

**Erwartet:** Eine Tabelle mit Minuten je Tag und Kategorie, eine Tabelle Schätzung gegen Messung. Bei Neles Beispieldatei: 1.340 Minuten gesamt; Fokusarbeit 720 (54 %), Abstimmung 270 (20 %), Kleinkram 350 (26 %). Montag 2026-09-28 hat 260 Minuten, Mittwoch 2026-09-30 hat 295 Minuten.
**Schreibgrenze:** Keine Datei. Die CSV-Datei bleibt unverändert.
**Selbst:** Die Summen von zwei Tagen selbst nachrechnen. Kriterium: Übereinstimmung auf die Minute; bei Abweichung die betroffene Zeile suchen. Die Abweichung zwischen Schätzung und Messung selbst deuten, in zwei Sätzen.

Danach in derselben Unterhaltung:

```text
Entwirf nach der Vorlage 03_Resources/Vorlagen/wochenplan.md einen Wochenplan für {Montag, JJJJ-MM-TT} bis {Freitag, JJJJ-MM-TT} und speichere ihn als 05_Daily/{Montag, JJJJ-MM-TT}-wochenplan.md. Ordne die offenen Board-Aufgaben nach Eisenhower ein und lege die wichtigen Aufgaben als Timeboxes in freie Fokus-Slots aus 03_Resources/Agent_Kontext/rhythmen.md. Lege für den Kleinkram ein Sammelfenster an, das zur Messung passt. Kennzeichne alles als Vorschlag und lass „Meine Entscheidung“ leer. Ändere keine andere Datei.
```

**Erwartet:** Feste Termine aus den Rhythmen, Timeboxes nur in Fokus-Slots ohne festen Termin, ein Sammelfenster mit Bezug zur Messung. „Meine Entscheidung“ ist leer.
**Schreibgrenze:** Eine neue Datei. Board, Protokoll und CSV-Datei unverändert.
**Selbst:** „Meine Entscheidung“ ausfüllen: streichen, verschieben oder bestätigen, je Änderung ein Satz Begründung. Die Prioritäten setzt die Person.
**Ins Protokoll:** Messung, Deutung und eine Zeile in einem Auftrag:

```text
Trage in docs/delegationsprotokoll.md bei „Gemessen“ ein: {Woche, Gesamtzeit, drei Anteile}. Trage bei „Meine Deutung“ wörtlich ein: {zwei eigene Sätze}. Hänge unten an die Tabelle unter „Einträge“ diese Zeile an: {Datum}, Zeiterfassung auswerten (Termin 2), {an den Agenten}, {selbst behalten}, {geprüft wie}, {Befund}. Ändere sonst nichts.
```

## Termin 3: Kanalarchitektur auf Lücken prüfen

**Voraussetzung:** Der Entwurf der Kanalarchitektur aus dem Playbook liegt als Text vor.

```text
Hier ist der Entwurf der Kanalarchitektur unseres Projektteams: {Text einfügen}. Spiele zehn typische Nachrichten aus unserem Projekt durch; den Kontext liefert 01_Projects/02_DWSC_Morgenrot/info_02.md. Nimm diese eigenen Beispiele dazu: {zwei bis drei Nachrichtentypen ohne Namen}. Nenne jede Nachricht, die nach diesen Regeln keinen klaren Ort hat, und welche Regel fehlt. Antworte als Tabelle im Chat und ändere keine Datei.
```

**Erwartet:** Eine Tabelle mit Nachricht, Grund für den fehlenden Ort und fehlender Regel. Die eigenen Beispiele sind enthalten.
**Schreibgrenze:** Keine Datei.
**Selbst:** Entscheiden, welche Lücke das Team schließen soll, und die neue Regel selbst formulieren. Die Wahl in einem Satz begründen und im Team vorschlagen.
**Ins Protokoll:** Aufgabe „Kanalarchitektur auf Lücken prüfen (Termin 3)“; im Befund notieren, welche genannte Lücke keine echte war.

## Termin 4: Mitschrift der zweiten Runde ins Projektlog

**Wann:** Nach dem Termin, bis zum nächsten Termin. Das Planspiel im Termin bleibt ungekürzt.
**Voraussetzung:** Die Mitschrift der zweiten Runde liegt in `00_Inbox/`, aufgebaut nach `03_Resources/Vorlagen/mitschrift.md`.

```text
Übernimm die Mitschrift 00_Inbox/{Dateiname}.md als neuen Logeintrag vom {JJJJ-MM-TT} unten in 01_Projects/02_DWSC_Morgenrot/info_02.md. Ein kurzer Absatz mit den Entscheidungen, wer was bis wann übernimmt (Vorname und Rolle), und ein Link auf die Mitschrift. Ändere sonst nichts, auch nicht das Board.
```

**Erwartet:** Ein neuer Eintrag `### JJJJ-MM-TT: …` am Ende des Logs, mit Link auf die Mitschrift. Offene Punkte sind als offen gekennzeichnet.
**Schreibgrenze:** Eine Datei, nur hinzugefügte Zeilen. Mitschrift und Board unverändert.
**Selbst:** Jede Aussage im Eintrag mit der Mitschrift vergleichen. Kriterium: Jede Entscheidung steht so in der Mitschrift. Den Eintrag zusätzlich gegen die KI-Regel für Meetings aus Playbook-Kapitel 2 prüfen.
**Ins Protokoll:** Aufgabe „Mitschrift Runde 2 ins Projektlog (Termin 4)“; im Befund jede Abweichung von der Mitschrift.

## Termin 5: Fertig-Kriterien gegenprüfen

**Voraussetzung:** Die Fertig-Kriterien aus dem Team-Board liegen als Text vor.

```text
Hier sind die Fertig-Kriterien unseres Team-Boards: {Text einfügen}. Nenne jedes Kriterium, das zwei Personen verschieden beurteilen könnten, und begründe das in einem Satz. Formuliere keine neue Fassung. Antworte als Tabelle im Chat und ändere keine Datei.
```

**Erwartet:** Eine Tabelle mit Kriterium und Begründung. Kein Vorschlag für eine Neufassung.
**Schreibgrenze:** Keine Datei. Das Team-Board bleibt unberührt.
**Selbst:** Die unklaren Kriterien selbst neu formulieren und die Änderung im Team begründen.
**Ins Protokoll:** Aufgabe „Fertig-Kriterien gegenprüfen (Termin 5)“; im Befund, welchem Einwand des Agenten Sie nicht folgen und warum.

## Termin 6: Durchsatz und Retro ins Projektlog

**Wann:** Nach dem Termin, bis zum nächsten Termin. Das Planspiel im Termin bleibt ungekürzt.

```text
Hänge unten in 01_Projects/02_DWSC_Morgenrot/info_02.md einen Logeintrag vom {JJJJ-MM-TT} zur Sprint-Simulation an. Inhalt: die drei Durchsatzwerte {Wert 1, Wert 2, Wert 3} und die Retro-Verbesserungen {…}. Übernimm darunter wörtlich meine Deutung: {zwei bis drei eigene Sätze}. Quelle ist dieser Auftrag. Ändere sonst nichts, auch nicht das Board.
```

**Erwartet:** Ein neuer Eintrag am Ende des Logs mit drei Werten, den Verbesserungen und der Deutung im eigenen Wortlaut.
**Schreibgrenze:** Eine Datei, nur hinzugefügte Zeilen.
**Selbst:** Die Deutung der Werte schreiben, bevor der Prompt abgeht. Danach prüfen. Kriterium: Werte und Deutung stehen unverändert im Eintrag.
**Ins Protokoll:** Aufgabe „Sprint-Werte ins Projektlog (Termin 6)“; im Befund, ob der Agent etwas umformuliert hat.

## Termin 7: OKR-Entwurf prüfen

**Voraussetzung:** Der OKR-Entwurf liegt als Text vor.

```text
Hier ist unser OKR-Entwurf: {Text einfügen}. Prüfe jedes Key Result mit zwei Fragen: Beschreibt es eine Tätigkeit oder ein Ergebnis? Fehlt ein Ausgangswert? Antworte als Tabelle im Chat, formuliere nichts um und ändere keine Datei.
```

**Erwartet:** Eine Tabelle mit je einer Zeile pro Key Result und einer Antwort auf beide Fragen.
**Schreibgrenze:** Keine Datei.
**Selbst:** Die Key Results selbst überarbeiten und den Ausgangswert aus eigenen Daten belegen.
**Ins Protokoll:** Aufgabe „OKR-Entwurf prüfen (Termin 7)“; im Befund jede Einordnung, die Sie anders sehen.

## Termin 8: Feedback zum Feedback ins Protokoll

Weg A im Termin (Gespräch mit »Alex«) zählt als Agenten-Auftrag. Ein neuer Prompt an den Agenten in der Ablage ist nicht nötig.

**Ins Protokoll:** Aufgabe „Feedback zum Feedback, Weg A (Termin 8)“. Im Befund notieren, was die KI richtig und was sie falsch gesehen hat.

> **Achtung:** Keine Namen mit Bewertungen ins Protokoll. Statt des Namens die Rolle nennen.

## Termin 9: Delegationsmatrix

Kein neuer Auftrag. Das [Delegationsprotokoll](delegationsprotokoll.md) zu Termin 9 mitbringen; die Zeilen der Delegationsmatrix entstehen aus den eigenen Einträgen.

## Klausur-Sprint mit NotebookLM

Ausblick in Termin 12. Im Klausur-Sprint dient NotebookLM zum Abfragen aus eigenem Material: Die eigenen Lernnotizen und Transfer-Memos werden hochgeladen, NotebookLM fragt daraus ab. Das Hochladen erledigt die Person selbst; der Agent in der Ablage lädt nichts hoch. Die Klausur selbst läuft ohne KI.
