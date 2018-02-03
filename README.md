# (1) SW-Entwicklung, -Wartung & (Re-)Engineering

## 1.2 SW-Qualität

- Qualität ist der Grad, indem ein System die Kundenerwartungen und Kundenbedürfnisse erfüllt.
- **Qualitätsmerkmale**: Funktionalität
- **Nichtfunktionale Merkmale**:
  - Zuverlässigkeit
  - Benutzbarkeit
  - Effizienz
  - Änderbarkeit
  - Übertragbarkeit

- **Prinzipien der QS**:
  - Qualitätszielbestimmung
  - quantitative QS (z.B durch Metriken)
  - konstruktive QS
    - technische Maßnahmen (z.B. IDE, Sprache, Tools)
    - organisatorische Maßnahmen (z.B DoD, Guidelines, Standards)
  - analytische QS
    - analysierende Verfahren (z.B reviews, static analysis, formal verification)
    - testende Verfahren (z.B. dynamische Tests, symbolische Tests)
  - unabhängige QS (durch QA-Team)

## 1.3 Iterative SW-Entwicklung

**Wasserfallmodell**<br>
<img src="./assets/wasserfall.PNG" width="500">

* Wasserfall ist **scheiße**, weil ...
    * strikte Phaseneinteilung ist unrealistisch
    * Anforderungen sind zu Beginn unklar und ändern sich ständig

**V-Modell**<br>
<img src="./assets/v-modell.PNG" width="500">

## 1.4 Forward-, Reverse- und Reengineering

Forward-Engineering<br>
<img src="./assets/forward-engineering.PNG" width="400">

Reverse-Engineering<br>
<img src="./assets/reverse-engineering.PNG" width="400">

Reengineering<br>
<img src="./assets/reengineering.PNG" width="400">

# (2) Konfigurationsmanagement

## 2.1 Einleitung

* **KM-Planung**: Beschreibung der Standards, Verfahren, Tools
* **Versionsmanagement**: Verwaltung der Entwicklungsgeschichte (git)
* **Variantenmanagement**: Verwaltung parallel existierender Ausprägungen eines Produkts für verschiedene Anforderungen, Länder, Plattformen etc.
* **Releasemanagement**: Verwaltung und Planung von Auslieferungsständen
* **Buildmanagement**: Erzeugung des auszuliefernden Produkts
* **Änderungsmanagement**: Verwaltung von Feature Requests

**Integration des KMs im V-Modell**<br>
<img src="./assets/km-v-modell.PNG" width="500">

## 2.2 Versionsmanagement

#### Source Code Control System (SCCS)

* Je Dokument gibt es eine eigene History-Datei, die alle Revisionen als eine Liste jeweils geänderter Blöcke speichert.

* **Instruktionen zur Erzeugung von Deltas (SCCS)**
    * Die Anzahl der geänderten, gelöschten und neu erzeugten Zeilen aller Hunks eines Deltas zweier Dateien wird möglichst **klein gehalten**.
    * Jeder Hunk beginnt mit genau **einer** unveränderten **Kontextzeile** und enthält sonst nur geänderte, gelöschte oder neu eingefügte Zeilen (Ausnahme: Dateianfang).
    * Aufeinander folgende Hunks sind also durch jeweils **mindestens eine unveränderte Zeile** getrennt.
    * Optional: Anstelle von Löschen und Neuerzeugen einer Zeile `i` verwendet man die **Änderungsmarkierung** `"!"`
* SCCS ist nicht gut da **single write access** und **multiple read access**

#### Revision Control System (RCS)

* Je Dokument gibt es eine eigene History-Datei, die eine neueste Revision vollständig und andere Revisionen als Deltas speichert

* Problem: kein Konfigurationsbegriff und kein Variantenbegriff

#### Concurrent Version System (CVS)

* Reimplementierung von RCS
* merge-Konzept (merge-conflicts muss der Entwickler manuell beheben)
* Releasemanagement mit Hilfe von Tags
* Hilfsprogramme wie z.B. "cvsann" (wie eine git-blame annotation)
* Problem: 
    * keine Versionierung von Directories
    * zugeschnitten auf Textdateien
    * nicht gut für verteilte SW-Entwicklung

#### Subversion (SVN)

* löst die Probleme von CVS

#### Prinzipien echt verteilter Versionierungs-Systeme (Git)

* Jeder Entwickler hat ein lokales Repository
* `checkout`, `commit`, etc. arbeiten auf der lokalen Umgebung
* Austausch zwischen Repositories erfolgt mit `push` und `pull` per ssh oder http
* Bei Push/Pull werden parallele Revisionen angelegt, die dann mit `merge` zusammengeführt werden.

## 2.3 Variantenmanagement (SW-Produktlinien)

// TODO: wtf

## 2.4 Releasemanagement

* Festlegung der Funktionalität eines neuen Releases
* Festlegung des Zeitpunktes der Freigabe eines neuen Releases
* Erstellung und Verbreitung eines Releases
* Dokumentation des Releases

#### Planungsprozess für neues Release

* Vorbedingungen für neues Release werden überprüft
    * viel Zeit vergangen
    * viele Fehler behoben
    * viele neue Funktionen hinzugefügt
* Weiterentwicklung wird eingefroren
    * **Feature Freeze** (soft freeze)
        * nur noch Bug- und Smallfixes
    * **Code Freeze** (hard freeze)
        * nur noch absolut notwendige Änderungen
* Letzte Fehlerkorrekturen und Tests werden durchgeführt
* Release wird freigegeben und deployed
    * Weiterentwicklung neuer Releases wird aufgenommen
    * freigegebenes Release muss parallel dazu gepflegt werden

## 2.5 Buildmanagement

* Werkzeuge für Buildmanagement
    * make
    * Ant
    * gradle
    * Maven
    * Jenkins

## 2.6 Änderungsmanagement

Heute läuft es folgendermaßen ab:
* Der Kunde hat ein feature request und wenn dieser sinnvoll ist, ensteht ein JIRA Item. Dieser wird bearbeitet und bei Sprint-Ende released. Fertig.