# Delegationsprotokoll

Das Protokoll hält fest, was an den Agenten ging, was die Person selbst behielt und wie sie prüfte. Die Spalte „Befund“ nennt, wo der Agent danebenlag; ohne Fehler steht dort „kein Fehler gefunden“. Etwa drei Einträge pro Woche ab dem Werkzeugtermin genügen.

**Fiktives Beispiel von Nele.** Beim ersten eigenen Eintrag (Demo-Drehbuch, Auftrag 3) werden Neles Zeilen ersetzt. Der Agent schreibt hier nur auf ausdrücklichen Auftrag (siehe [AGENTS.md](../AGENTS.md)).

## Schätzung vor der Zeiterfassung

Nele, 2026-09-24, vor dem ersten Eintrag der Zeiterfassung:

- Fokusarbeit: 65 %
- Abstimmung: 15 %
- Kleinkram: 20 %

**Gemessen** (Auswertung in Termin 2, Woche 2026-09-24 bis 2026-09-30, 22 Stunden 20 Minuten, [Beispieldatei](../00_Inbox/zeiterfassung-beispielwoche.csv)): Fokusarbeit 54 %, Abstimmung 20 %, Kleinkram 26 %.

**Meine Deutung:** Der Kleinkram füllt vor allem die halben Stunden nach den Fokus-Slots. Ich sammle ihn ab jetzt in einem festen Fenster am Nachmittag.

## Einträge

| Datum | Aufgabe | an den Agenten | selbst behalten | geprüft wie | Befund |
|---|---|---|---|---|---|
| 2026-09-24 | Persona eintragen (Erste Schritte, Schritt 5) | Angaben in die Vorlage `persona.md` übertragen | Ziel für das Semester und Ton selbst formuliert | Über Review den Diff gelesen; Files Changed nennt nur `persona.md` | Der Agent hatte unter „Arbeitsweise“ einen Satz ergänzt, der nicht in meinen Angaben stand. Per Folgeauftrag entfernt. |
| 2026-10-01 | Zeiterfassung der Woche ab 2026-09-24 auswerten (Termin 2) | Summen je Tag und Kategorie, Anteile, Vergleich mit der Schätzung | Deutung der Abweichung, Folgerung für den Wochenplan | Summen für Montag und Mittwoch selbst nachgerechnet | Montag um 20 Minuten zu hoch: Die Zeile 13:15 bis 13:35 war doppelt gezählt. Mittwoch stimmte. |
| 2026-10-02 | Tagesnotiz [2026-10-02](../05_Daily/2026-10-02.md) vorbereiten | Vorschlag für Prioritäten, Termine, Board-Auszug | Auswahl der drei Prioritäten | Termine mit `rhythmen.md` und den Auszug mit dem Board verglichen | Der Agent schrieb „keine Termine, Tag frei“. Korrigiert: Ohne Kalenderzugriff gilt kein Tag als frei. |

## Einen Eintrag ergänzen

Voraussetzung: Der Auftrag ist erledigt und das Ergebnis geprüft.

1. Beginnen Sie über **New Conversation** eine neue Unterhaltung im Projekt.
2. Kopieren Sie den Prompt und füllen Sie die Platzhalter in eigenen Worten.

   ```text
   Hänge in docs/delegationsprotokoll.md unten an die Tabelle unter „Einträge“ eine Zeile an: Datum {JJJJ-MM-TT}, Aufgabe {…}, an den Agenten {…}, selbst behalten {…}, geprüft wie {…}, Befund {…}. Übernimm meine Angaben wörtlich. Ändere keine andere Zeile und keine andere Datei.
   ```

3. Schicken Sie den Prompt ab.
4. Öffnen Sie über **Review** den Diff.
5. Prüfen Sie das Ergebnis. Kriterium: genau eine hinzugefügte Zeile, keine entfernte Zeile, nur diese Datei geändert.

## Weiter in Termin 9

In Termin 9 (Delegationsmatrix-Werkstatt) entstehen die Zeilen der Delegationsmatrix aus den eigenen Einträgen. Bringen Sie das Protokoll deshalb zu Termin 9 mit.
