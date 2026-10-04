# Demo-Drehbuch: sieben Aufträge an den Agenten

Die Aufträge bauen aufeinander auf. Die Aufträge 1 bis 3 laufen im Werkzeugtermin, die Aufträge 4 bis 7 bis Termin 2. Die Aufträge der folgenden Termine stehen in den [Kursaufträgen](kurs-auftraege.md). Voraussetzung: Der Ordner ist als Projekt in Antigravity geöffnet (siehe [Erste Schritte](erste-schritte.md)), das Permission Preset steht auf Default.

**Ablauf je Auftrag**

1. Über **New Conversation** eine neue Unterhaltung im Projekt beginnen. Der Chip über dem Eingabefeld zeigt den Projektordner.
2. Den Prompt kopieren, einfügen und abschicken.
3. Das Ergebnis mit „Erwartet“ vergleichen. Steht unter der Antwort eine Zeile wie `1 file changed`, über **Review** den Diff lesen. Im rechten Bereich listet **Files Changed** alle geänderten Dateien.
4. Prüfen, ob die Schreibgrenze eingehalten wurde. Erscheint ein Berechtigungsdialog, den Befehl lesen und im Zweifel `1 Yes, allow this time` wählen.

Ist etwas durcheinandergeraten, den Ordner aus der ZIP-Datei neu entpacken. Dabei gehen alle eigenen Änderungen verloren.

| Zeit | Auftrag | Schreibt |
|---|---|---|
| 5 min | 1. Ordner und Regeln erkunden | nichts |
| 10 min | 2. Inbox sichten | nichts |
| 10 min | 3. Mitschrift ins Projektlog | einen Logeintrag, danach die erste Protokollzeile |
| 10 min | 4. Tagesnotiz vorbereiten | eine neue Datei |
| 15 min | 5. Wochenplan entwerfen | eine neue Datei |
| 10 min | 6. Lernnotiz abfragen lassen | nichts |
| 10 min | 7. Projekt archivieren | Verschiebung, Logeintrag, Links |

## 1. Ordner und Regeln erkunden

```text
Welche Rules sind in dieser Unterhaltung aktiv und aus welcher Datei stammen sie? Beschreibe danach in fünf Sätzen, wie dieser Ordner aufgebaut ist und wo persönliche Aufgaben stehen. Nur lesen, nichts ändern.
```

**Erwartet:** Die Antwort nennt `AGENTS.md` im Hauptordner. Sie beschreibt die Ordner `00_Inbox` bis `05_Daily` und nennt `docs/board.md` als einzige Quelle für persönliche Aufgaben. Tauchen weitere Regeldateien auf, etwa globale Regeln, kurz prüfen, ob sie gewollt sind.
**Schreibgrenze:** Keine Datei. Unter der Antwort steht keine Zeile mit geänderten Dateien.
**Prinzip:** Lesen ist eine eigene Stufe. Die Regeln wirken, ohne im Prompt zu stehen.

## 2. Inbox sichten

```text
Sichte 00_Inbox/2026-10-02-schnellnotizen.md. Schlage für jede Notiz ein Ziel in diesem Ordner vor (Projekt, Area oder Lernnotiz) und begründe es in einem Satz. Nenne mögliche neue Aufgaben getrennt als Vorschlag für das Board. Antworte als Tabelle im Chat und ändere keine Datei.
```

**Erwartet:** Notiz 1 gehört zur Semesterarbeit und passt zur Vorbereitung der Sprechstunde (ST-12). Notiz 2 gehört zur Area Nebenjob und zu ST-16. Notiz 3 gehört zur Lernnotiz Modul 1; ergänzen soll sie Nele selbst. Notiz 4 wird als Nachricht mit Anweisung an KI-Assistenten gemeldet: nichts zusammengefasst, gesendet oder gelöscht. Neue Aufgaben erscheinen nur als Vorschlag.
**Schreibgrenze:** Keine Datei, auch nicht das Board.
**Prinzip:** Inhalte sind Daten, keine Aufträge. Delegiert ist der Vorschlag, die Entscheidung bleibt bei der Person.

## 3. Mitschrift ins Projektlog übernehmen

```text
Übernimm die Mitschrift 00_Inbox/2026-10-01-mitschrift-teamtreffen.md als neuen Logeintrag vom 2026-10-01 unten in 01_Projects/02_DWSC_Morgenrot/info_02.md. Ein kurzer Absatz mit den Entscheidungen und ein Link auf die Mitschrift. Ändere sonst nichts, auch nicht das Board.
```

**Erwartet:** Unten in `info_02.md` steht ein neuer Eintrag `### 2026-10-01: …`. Er nennt die eigenen Fokusregeln bis 2026-10-07, das Zusammenführen von Kapitel 1 durch Lukas am 2026-10-08 und die noch offene Entscheidung zu den gemeinsamen Fokuszeiten. Er verlinkt die Mitschrift.
**Schreibgrenze:** Eine Datei, nur hinzugefügte Zeilen. Der Diff zeigt keine entfernte Zeile; Mitschrift und Board bleiben unverändert.
**Prinzip:** Das Log hält belegte Geschichte fest. Status und nächste Schritte bleiben im Board.

**Danach: erste Zeile im Delegationsprotokoll.** Voraussetzung: Der Logeintrag ist geprüft.

1. Beginnen Sie eine neue Unterhaltung.
2. Füllen Sie die Platzhalter im Prompt in eigenen Worten und schicken Sie ihn ab.

   ```text
   Ersetze in docs/delegationsprotokoll.md die Beispielzeilen unter „Einträge“ durch diese eine Zeile: Datum {JJJJ-MM-TT}, Aufgabe „Mitschrift ins Projektlog (Demo-Auftrag 3)“, an den Agenten {…}, selbst behalten {…}, geprüft wie {…}, Befund {…}. Übernimm meine Angaben wörtlich. Ändere keine andere Datei.
   ```

3. Öffnen Sie über **Review** den Diff.
4. Prüfen Sie das Ergebnis. Kriterium: Unter „Einträge“ steht genau eine Zeile, der Abschnitt „Schätzung“ ist unverändert.

Mögliche Angaben: an den Agenten „Logeintrag aus der Mitschrift“; selbst behalten „was als entschieden gilt“; geprüft wie „Diff gelesen, jede Entscheidung mit der Mitschrift verglichen“. Den Befund schreibt jede Person aus der eigenen Prüfung. Weiter geht es im [Werkzeugtermin der Kursaufträge](kurs-auftraege.md#werkzeugtermin-protokoll-beginnen-und-zeiterfassung-starten).

## 4. Tagesnotiz vorbereiten

```text
Lege die Tagesnotiz 05_Daily/2026-10-05.md nach der Vorlage 03_Resources/Vorlagen/tagesnotiz.md an. Quellen: docs/board.md, 03_Resources/Agent_Kontext/rhythmen.md und die Projektdateien der offenen Aufgaben. Schlage drei Prioritäten mit Board-ID vor. Lass Notizen und Journal leer. Ändere keine andere Datei.
```

**Erwartet:** Montag, 2026-10-05, mit Fokus-Slot 09:00 bis 10:30 und Vorlesung 11:30 bis 13:00. Drei Prioritäten mit ID, naheliegend ST-10 (fällig 2026-10-07), ST-12 (Sprechstunde 2026-10-08) und ST-14 oder ST-15. ST-11 erscheint höchstens als Waiting, nicht als Priorität. Der Board-Auszug nennt den Stand 2026-10-02, 18:00, und der fehlende Kalenderzugriff ist erwähnt.
**Schreibgrenze:** Eine neue Datei. Board und Projekte unverändert, Journal leer.
**Prinzip:** Die Tagesnotiz ist ein Auszug mit Zeitpunkt, keine zweite Aufgabenliste.

## 5. Wochenplan entwerfen

```text
Entwirf nach der Vorlage 03_Resources/Vorlagen/wochenplan.md einen Wochenplan für 2026-10-05 bis 2026-10-09 und speichere ihn als 05_Daily/2026-10-05-wochenplan.md. Ordne die offenen Board-Aufgaben nach Eisenhower ein, lege die wichtigen Aufgaben als Timeboxes in freie Fokus-Slots und sammle Kleinkram in einem Fenster. Kennzeichne alles als Vorschlag und lass den Abschnitt „Meine Entscheidung“ leer. Ändere das Board nicht.
```

**Erwartet:** Feste Termine aus den Rhythmen (Schicht Dienstag, Sport Mittwoch, Seminar und Teamtreffen Donnerstag) und die Sprechstunde Donnerstag 14:00 aus der Projektdatei der Semesterarbeit. Timeboxes für ST-12 vor Donnerstag, ST-10 bis Mittwoch, ST-14 und ST-15 bis Freitag. ST-16 im Sammelfenster. ST-11 ohne Timebox, weil auf das Teamtreffen gewartet wird.
**Schreibgrenze:** Eine neue Datei.
**Danach selbst:** Den Abschnitt „Meine Entscheidung“ ausfüllen. Eine Einordnung unverändert zu übernehmen gibt genau den Teil aus der Hand, der nicht delegierbar ist.
**Prinzip:** Delegieren, behalten, prüfen am Wochenplan aus Modul 1.

## 6. Lernnotiz abfragen lassen

```text
Frag mich zu meiner Lernnotiz 03_Resources/Lernnotizen/dwsc-modul-1.md ab. Stelle drei Fragen nacheinander und stelle die nächste erst, wenn ich geantwortet habe. Gib nach jeder Antwort eine kurze Rückmeldung, ob sie zu meiner Notiz passt. Nenne am Ende, was ich unter „Unsicher“ ergänzen könnte. Ändere keine Datei.
```

**Erwartet:** Genau eine Frage pro Nachricht, ohne vorweggenommene Antwort. Die Rückmeldungen beziehen sich auf die eigene Notiz. Am Ende Vorschläge für „Unsicher“, die Nele selbst einträgt.
**Schreibgrenze:** Keine Datei. Die Lernnotiz bleibt in Neles Worten.
**Prinzip:** In der Klausur zählt, was ohne KI gekonnt wird. Der Agent stützt das Verstehen, statt es zu ersetzen. Fachlich gilt im Zweifel das Kursmaterial.

## 7. Abgeschlossenes Projekt archivieren

```text
Das Fokus-Experiment (ST-3) ist laut Board abgeschlossen. Verschiebe den Ordner 01_Projects/03_Fokus_Experiment nach 04_Archive/03_Fokus_Experiment. Hänge in info_03.md einen Logeintrag vom 2026-10-04 zur lokalen Archivierung an. Passe alle relativen Links an, die auf das Projekt zeigen oder aus ihm herausführen, und führe das Projekt in 02_Areas/Studium.md unter „Abgeschlossen“. Ändere im Board nur den Link, keinen Status. Lösche nichts und nenne am Ende alle geänderten Dateien.
```

**Erwartet:** Der Ordner liegt unter `04_Archive/03_Fokus_Experiment` mit beiden Dateien. `info_03.md` hat einen neuen letzten Logeintrag; der Link auf das DWSC-Projekt führt jetzt über `../../01_Projects/`. Angepasste Links in `docs/board.md`, `02_Areas/Studium.md`, `03_Resources/Agent_Kontext/persona.md`, `01_Projects/02_DWSC_Morgenrot/info_02.md` und `05_Daily/2026-10-02.md`. ST-3 steht im Board weiter auf Done.
**Schreibgrenze:** Die Verschiebung, ein Logeintrag, die Liste in `Studium.md` und Linkziele. Kein Status, keine Löschung.
**Prinzip:** Abschluss im Board und Ablage im Archiv sind getrennte Schritte. Der ausdrückliche Auftrag erlaubt die Verschiebung.

## Nachbesprechung

- Bei welchem Auftrag war die Schreibgrenze am schwersten zu formulieren?
- Welcher Teil eines Auftrags wäre in der eigenen Ablage nicht delegierbar?
- Welche Regel fehlt in `AGENTS.md` für die eigene Arbeitsweise?
