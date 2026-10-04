# Erste Schritte

Benötigt wird nur die App Antigravity mit Anmeldung über ein Google-Konto. Kein Git, kein Terminal, keine weitere Installation.

## Einrichtung in fünf Schritten

**1. ZIP entpacken.** Die ZIP-Datei [second-brain-studium.zip](https://github.com/kirenz/second-brain-studium/releases/latest/download/second-brain-studium.zip) herunterladen und entpacken, zum Beispiel in den Ordner Dokumente. Es entsteht der Ordner `second-brain-studium`. Die ZIP-Datei aufbewahren: Mit ihr lässt sich der Ausgangszustand jederzeit wiederherstellen.

**2. Antigravity vorbereiten.** Die App starten und mit dem Google-Konto anmelden, für das das KI-Abo gilt. Unter **Settings**, **Models** stehen bei **Models & Usage** der Plan und das verbleibende Kontingent. Unter **Settings**, **General** das **Permission Preset** auf **Default** lassen; **Turbo** nicht für diesen Ordner verwenden.

**3. Ordner als Projekt öffnen.** In der Seitenleiste neben **Projects** das Symbol **Create New Project** anklicken, **New Project** wählen und im Ordnerdialog `second-brain-studium` auswählen. Über dem Eingabefeld erscheint der Chip `second-brain-studium`.

**4. Ersten Auftrag stellen.** Eine neue Unterhaltung beginnen und senden:

```text
Welche Rules sind in dieser Unterhaltung aktiv und aus welcher Datei stammen sie? Beschreibe danach kurz, wie dieser Ordner aufgebaut ist. Nur lesen, nichts ändern.
```

Die Antwort nennt `AGENTS.md`. Damit ist klar, dass der Agent die Regeln dieses Ordners kennt. Im Verlauf über der Antwort zeigen Schritte wie `Analyzed AGENTS.md`, welche Dateien gelesen wurden.

**5. Persona ersetzen.** In einer neuen Unterhaltung die eigenen Angaben eintragen lassen und das Ergebnis über **Review** prüfen:

```text
Ersetze in 03_Resources/Agent_Kontext/persona.md die Beispielperson durch diese Angaben: Vorname {…}, Studiengang und Semester {…}, Bereich im DWSC-Projektteam {…}, daneben {Nebenjob, Ehrenamt oder anderes}, Ziel für das Semester {…}. Behalte Aufbau und Abschnitte bei. Ändere keine andere Datei.
```

Ein Vorname genügt. Matrikelnummer, Adresse, Telefonnummer und Gesundheitsangaben gehören nicht in die Ablage.

Danach eignet sich das [Demo-Drehbuch](demo-drehbuch.md), um die Arbeitsweise an den Beispieldaten auszuprobieren, bevor eigene Inhalte folgen. Ab Termin 2 gibt es je Termin einen Auftrag in den [Kursaufträgen](kurs-auftraege.md).

## Was der Agent im Ordner darf

Lesen und Schreiben im geöffneten Projektordner laufen in der Regel ohne Rückfrage. Die Grenze setzt deshalb der Auftrag: Er nennt, welche Datei geändert werden darf, oder sagt „nichts ändern“. Nach jedem Auftrag zeigt eine Zeile wie `1 file changed` mit der Schaltfläche **Review**, was sich geändert hat. Für Zugriffe außerhalb des Ordners fragt der Agent im Preset Default nach. Laufende Arbeit hält die rote Stopp-Schaltfläche an.

Deshalb nur Inhalte in den Ordner legen, die der Agent sehen darf.

## Eigene Ablage aufbauen

Die Beispielinhalte schrittweise durch eigene ersetzen, in dieser Reihenfolge:

1. **Rhythmen:** In `03_Resources/Agent_Kontext/rhythmen.md` den eigenen Stundenplan, Schichten und Fokus-Slots eintragen. Diese Datei ist die Terminquelle für Tagesnotiz und Wochenplan.
2. **Projekte:** Das DWSC-Projekt behalten und Teamname, Bereiche und Vornamen anpassen. Für jedes weitere Vorhaben mit Ende einen Ordner nach `03_Resources/Vorlagen/projekt.md` anlegen lassen, zum Beispiel:

   ```text
   Lege nach der Vorlage 03_Resources/Vorlagen/projekt.md das Projekt 01_Projects/06_{Name}/info_06.md an. Angaben: {Fach, Ziel, Abgabe}. Trage im Board unter Projekte die Zeile ST-6 ein. Ändere sonst nichts.
   ```

3. **Board:** In `docs/board.md` die Beispielaufgaben durch eigene ersetzen. Jede Aufgabe ist ein konkreter nächster Schritt mit Status und Fälligkeit. Teamaufgaben bleiben im Team-Board des Kurses.
4. **Areas:** Die drei Beispieldateien anpassen oder ersetzen, etwa durch Finanzen oder Ehrenamt. Eine Area hat kein Enddatum.
5. **Lernnotizen:** Für jedes Klausurmodul eine Notiz nach `03_Resources/Vorlagen/lernnotiz.md` selbst schreiben. Der Agent fragt ab, formuliert aber nicht.
6. **Delegationsprotokoll:** Neles Beispielzeilen in `docs/delegationsprotokoll.md` durch eigene ersetzen lassen. Den Prompt dafür enthält Auftrag 3 im Demo-Drehbuch. Ab dann etwa drei Einträge pro Woche ergänzen.
7. **Aufräumen:** Beispielprojekte, Inbox-Beispiele samt Zeiterfassung und die Beispiel-Tagesnotiz selbst im Finder oder Explorer löschen, sobald sie nicht mehr gebraucht werden. Der Agent löscht laut `AGENTS.md` nichts.
8. **Regeln:** Eigene Dauerregeln knapp in `AGENTS.md` ergänzen, etwa Abgabezeiten oder die KI-Regeln eines Fachs. Kurze Regeln wirken besser als lange; eine Rules-Datei wird nur bis 24 KB gelesen.

**Nicht in die Ablage:** Passwörter und Zugangsdaten, Matrikelnummer, Adressen und Telefonnummern, Gesundheitsdaten, Daten anderer Personen über Vorname und Rolle hinaus. Ob und wie KI in einer Prüfungsleistung genutzt werden darf, regelt das jeweilige Fach; diese Klärung gehört vor die erste Nutzung.
