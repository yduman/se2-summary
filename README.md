# Kapitel 0

### Wissensgebiete der Software-Technik
1) Software Requirements
    * festlegen **was** ein Software-System leisten soll
2) Software Design
    * Festlegung einer Architektur
3) Software Construction
    * Realisierung der Software
4) Software Testing
    * Fehler werden systematisch gesucht und eliminiert
5) Software Maintanence
    * Pflege und Weiterentwicklung der Software nach Auslieferung
6) Software Configuration Management
    * Verwaltung von Software-Versionen und -Konfigurationen
7) Software Engineering Management
    * Projektmanagement von Personen, Organisationen und Zeitplänen
8) Software Engineering Process
    * Definition und Verbesserung von Entwicklungsprozessen
9) Software Engineering Models and Methods
    * Modelle und Methoden für die Software-Entwicklung
10) Software Quality
    * Messen und Verbessern der Software-Qualität

# Kaptitel 1: Software-Entwicklung, -Wartung und Engineering

## Einleitung

* **Software-Engineering** ist die Entwicklung die Pflege und der Einsatz qualitativ hochwertiger Software unter Einsatz von
    * wissenschaftlichen Methoden
    * wirtschaftlichen Prinzipien
    * geplanten Vorgehensmodellen
    * Werkzeugen
    * quantifizierbaren Zielen

## Sofware-Qualität

**Ziel der Software-Technik** ist die effiziente Entwicklung messbar qualitativ hochwertiger Software, die
    * gewünschte Funktionalität anbietet
    * benutzerfreundliche Oberfläche besitzt
    * korrekt bzw. zuverlässig arbeitet

#### Qualitätsmerkmale
* Funktionalität
* Zuverlässigkeit
* Benutzbarkeit
* Effizienz
* Änderbarkeit
* Übertragbarkeit

#### Prinzipien der Qualitätssicherung
* Qualitätszielbestimmung
* quantitative QS 
    * Einsatz von Metriktools
* konstruktive QS
    * Verwendung geeigneter Methoden, Sprachen und Werkzeuge
* integrierte, frühzeitige analystische QS
    * systematische Prüfung aller erzeugten Dokumente
* unabhängige QS
    * Überprüfung durch eigenständige QS-Abteilung

#### Konstruktives Qualitätsmanagement zur Fehlervermeidung
* **technische Maßnahmen**
    * Sprachen (UML, Java etc.)
    * Tools (IDE, UML-Tools etc.)
* **organisatorische Maßnahmen**
    * Richtlinien
    * Standards
    * Checklisten

#### Analytisches Qualitätsmanagement zur Fehleridentifikation
* **analysierende Verfahren**
    * Review
    * statische Analyse
    * formale Verifikation
* **testende Verfahren**
    * dynamischer Test (normale Ausführung mit ganz konkreten Eingaben)
    * symbolischer Test

## Iterative Software-Entwicklung

* **Wasserfallmodell** (just don't do this)
    * **Probleme**
        * zu Projektbeginn sind ungenaue Kosten- und Ressourcenabschätzung möglich
        * ein Pflichtenheft kann nie den Umgang mit dem fertigen System ersetzen
        * Anforderungen werden früh eingefroren, notwendiger Wandel nicht eingeplant
        * ...

* **Das V-Modell**

* **Scrum**

* **XP**

## Forward-, Reverse- und Reengineering

#### Forward Engineering

* Beim **Forward Engineering** ist das fertige Softwaresystem das Ergebnis des Entwicklungsprozesses.
* **Anforderungen** --> **Design** --> **Code**

#### Reverse Engineering
* Beim **Reverse Engineering** ist das vorhandene System der Ausgangspunkt der Analyse. Ausgehend von existierender Implementierung wird meist nur das Design rekonstruiert und dokumentiert. Es wird (noch) nicht das betrachtete System modifiziert.
* **Anforderungen** <-- **Design** <-- **Legacy-Code**

#### Reengineering
* Reengineering befasst sich mit der Software-Sanierung. Dabei werden Ergebnisse des Reverse Engineerings als Ausgangspunkt genommen.

# Kapitel 2

## Konfigurationsmanagement (KM)

Beim Konfigurationsmanagement handelt es sich um die Entwicklung und Anwendung von Standards und Verfahren zur Verwaltung eines sich weiterentwickelnden Systems.

#### Werkzeugorientierte Sicht auf KM-Aktivitäten

* **KM-Planung**
    * Beschreibung der Standards, Verfahren und Werkzeuge, die für KM benutzt werden; wer darf/muss wann was machen
* **Versionsmanagement**
    * Verwaltung der Entwicklungsgeschichte eines Produkts; also wer hat wann, wo, was und warum geändert
* **Variantenmangement**
    * Verwaltung parallel existierender Ausprägungen eines Produkts für verschiedene Anforderungen, Länder, Plattformen
* **Releasemangement**
    * Verwaltung und Planung von Auslieferungsständen; wann wird eine neue Produktversion mit welchen Features auf den Markt geworfen
* **Buildmanagement**
    * Erzeugung des auszuliefernden Produkts; wann muss welche Datei mit welchem Werkzeug generiert, übersetzt, ... werden
* **Änderungsmanagement**
    * Verwaltung von Änderungsanforderungen; also Bearbeitung von Fehlermeldungen und Änderungswünschen (Feature Requests) sowie Zuordnung zu Auslieferungsständen


test
