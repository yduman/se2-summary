# Kapitel 0: Wissensgebiete der Software-Technik
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

# Kapitel 2: Konfigurationsmanagement (KM)

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

# Kapitel 3: Statische Programmanalyse und Metriken

Statische Codeanalyse verlangt ein stures, monotones Anwenden von relativ einfachen Regeln auf oft umfangreichen Code. Diese Aufgabe erfordert keinerlei Kreativität aber eine sehr große Übersicht und Kontrolle. [...] Statische Codeanalyse ist daher prädestiniert zur Automatisierung durch Werkzeuge. Ich empfehle Ihnen, diese Techniken entweder werkzeuggestützt oder gar nicht einzusetzen.

## Einleitung

* Oft finden sich 80% aller Probleme mit einem Softwaresystem in 20% des entwickelten Codes.
* Die statische Programmanalyse versucht meist diese 20% frühzeitig zu finden.
* Statische Analyseverfahren identifizieren Programmteile von fragwürdiger Qualität
* Statische Analyseverfahren versuchen die Qualität von Software zu messen

#### Analytisches Qualitätsmanagement zur Fehleridentifikation

* **analysierende Verfahren**
    * Review (durch Menschen)
    * statische Analyse (durch Werkzeug)
    * formale Verifikation (durch Werkzeug)
* **testende Verfahren**
    * dynamischer Test: "normale" Ausführung mit ganz konkreten Eingaben
    * symbolischer Test: Ausführung mit symbolischen Eingaben

#### Arten der Programmanalyse

* Visualisierung von Programmstrukturen
* manuelle Reviews
* Compilerprüfungen
* Programmverifikation und symbolische Ausführung
* Stilanalysen
* Kontroll- und Datenflussanalysen
* Metriken

## Softwarearchitekturen und -visualisierung

Große System sind immer in Subsysteme gegliedert, von denen jedes eine Anzahl von Diensten bereitstellt.

* **Begriffe nach Sommerville**
    * Ein Softwaresystem besteht aus Teilsystemen, die zusammengehörige Gruppen von Diensten anbieten und möglichst unabhängig voneinander realisiert sind.
    * Ein Teilsystem kann wiederum aus Teilsystemen aufgebaut werden, die aus Modulen bestehen.
    * Ein Modul bietet über seine Schnittstelle Dienste an und benutzt zu ihrer Realisierung Dienste anderer Module.
    * Ein Modul fasst "verwandte" Prozeduren, Klassen, ... zusammen.

## Strukturierte Gruppenprüfungen (Reviews)

* **Inspektion**: start formalisiertes Verfahren bei dem ein Dokument nach genau festgelegter Weise durch Gutachterteam untersucht wird.
* **Technisches Review**: weniger formale manuelle Prüfmethode; weniger Aufwand als bei Inspektion, ähnlicher Nutzen
* **Informelles Review (Walkthrough)**: unstrukturiertere Vorgehensweise; Autor des Dokuments liest vor, Gutachter stellen spontan Fragen
* **Pair Programming**: Programm wird von vornherein zu zweit erstellt.

## Kontroll- und Datenflussorientierte Analysen

Der Kontrollflussgraph ist [...] eine häufig verwendete Methode zur Darstellung von Programmen. [...] Die Verarbeitungssteuerung übernehmen die Kontrollstrukturen der Software unter Nutzung der Datenwerte. Eingabedaten werden gelesen, um Zwischenergebnisse zu bestimmen, die in den Speicher geschrieben werden, [...]. Die Daten "fließen" quasi durch die Software; von Eingaben zu Ausgaben.

#### Datenfluss- und Kontrollflussanomalien

Eine Anomalie eines Programms ist eine verdächtige Stelle in dem Programm. Eine solche Stelle ist keine garatiert fehlerhafte Stelle, aber eine potentiell fehlerhafte Stelle im Programm.

* **Datenflussanomalien** sind etwa:
    * es gibt einen Pfad im Kontrollflussgraphen, auf dem eine Variable v referenziert wird bevor sie zum ersten Mal definiert wird (Zugriff auf undefinierte Variable)
    * es gibt einen Pfad im Kontrollflussgraphen, auf dem eine Variable v zweimal definiert wird ohne zwischen den Definitionsstellen referenziert zu werden (nutzlose Zuweisung an Variable)

* **Kontrollflussanomalien** sind bei modernen Programmiersprachen von geringerer Bedeutung. Im wesentlichen handelt es sich dabei bei Programmiersprachen ohne "goto"-Anweisungen um nicht erreibaren Code.

## Softwaremetriken

Die Definition von Software-Maßen basiert auf dem Wunsch, einen quantitativen Zugang zum abstrakten Produkt Software zu gewinnen. Dabei ist zwischen der Vermussung von Eigenschaften einer Software und der quantitativen Kontrolle des zugrundeliegenden Entwicklungsprozesses zu unterscheiden.

* **Produktmetriken** messen Eigenschaften der Software:
    * Qualität der Software
    * Einhaltung von Standards
* **Prozessmetriken** messen Eigenschaften des Entwicklungsprozesses:
    * Dauer oder Kosten der Entwicklung
    * Zufriedenheit des Kunden

#### Gewünschte Eigenschaften von Maß/Metrik

* **Einfachheit**: berechnetes Maß lässt sich einfach interpretieren (z.B. LoC)
* **Validität**: es besteht ein Zusammenhang zwischen der gemessenen Eigenschaft und der interessanten Eigenschaft
* **Stabilität**: gemessene Werte sind stabil gegenüber Manipulationen untergeordneter Bedeutung
* **Rechtzeitigkeit**: das Maß kann zu einem Zeitpunkt berechnet werden, zu dem es noch zur Steuerung des Entwicklungsprozesses hilfreich ist.
* **Reproduzierbarkeit**: am besten automatisch berechenbar ohne subjektive Einflussnahme des Messenden.

#### Maßskalen

* Nominalskala
* Ordinalskala
* Rationalskala

#### Maßzahlen

* Lines of Code (LOC)
    * LOC(Programmteil) = Anzahl der Knoten im Kontrollflussgraphen dazu
* Zyklomatische Zahl nach McCabe
    * ZZ(Programmteil) = |E| - |N| + 2k
        * |E| := Anzahl der Kanten von G
        * |N| := Anzahl der Knoten von G
        * k := Anzahl Zusammenhangskomponenten von G
    * Regel von McCabe
        * ZZ eines Teilprogramms sollte nicht höher als 10 sein, da sonst Programm zu komplex.
* Live Variable (LV)
    * LV(K) = durchschnittliche Summe lebendiger Variablen an allen Knoten von K
* Variablenspanne (VS)
    * VS(K) = durchschnittlicher Wert aller VS(v, n1, n2) != 0 für alle möglichen Kombinationen von Variablen v und Knotenpaaren n1, n2.

#### Metriken für OO-Programme

* high cohesion
* low coupling
* data abstraction, encapsulation

* LOCOM1 (Low Cohesion Metric)
    * P := Anzahl der Paare von Methoden ohne gemeinsame Attributzugriffe
    * Q := Anzahl der Paare von Methoden mit gemeinsamen Attributzugriffen
    * LOCOM1 = if P > Q then P - Q else 0
* LOCOM2 (Low Cohesion Metric)
    * m := Anzahl Methoden m_i einer Klasse
    * m(a_i) := Anzahl Methoden, die auf Attribut a_i zugreifen
    * n:= Anzahl Attribute a_i einer Klasse
    * LOCOM2 = 1 - (m(a_1) + ... + m(a_a)) / (m * n)
    * gewünscht ist ein kleiner Wert von LOCOM2 (z.B < 0,3)

#### Kopplung von Klassen

* Afferent Coupling (AC)
    * Die Anzahl der Klassen ausserhalb eines betrachteten Teilsystems, die von den Klassen innerhalb des Teilsystems abhängen.
* Efferent Coupling (EC)
    * Die Anzahl der Klassen innerhalb eines betrachteten Teilsystems, die von Klassen ausserhalb des betrachteten Teilsystems abhängen
* Instabilität (I)
    * I = EC / (EC + AC)
* Coupling als Change Dependency between Classes (CDBC)
    * CDBC zwischen Client Class CC und Server Class SC :=
        * n falls SC Oberklasse von CC ist (n = Anzahl Methoden in CC)
        * n falls CC ein Attribut des Typs SC hat
        * j falls SC in j Methoden von CC benutzt wird
        * CDBC bewertet Aufwand, der mit Änderung der Klasse SC in CC verbunden sein könnte (sollte möglichst gering sein).
* Encapsulation als Attribute Hiding Factor (AHF)
    * Summer der Unsichtbarkeiten aller Attribute in allen Klassen geteilt druch die Anzahl aller Attribute
    * Unsichtbarkeit eines Attributs := Prozentzahl der Klassen, für die das Attribut nciht sichtbar ist (abgesehen von eigener Klasse)
    * sind alle Attribute als private definiert, dann ist AHF = 1
* Tiefe von Vererbungshierarchien
* Breite von Vererbungshierarchien
* Anzahl Redefinitionen in einer Klassenhierarchie
* Anzahl Zugriffe auf geerbte Attribute
* Halstead-Metriken
* ...

#### Komplexitätsmaße

* Response For Class (RFC)
    * die Anzahl der in der Klasse deklarierten methoden + die Anzahl der geerbten methoden + die Anzahl sichtbarer methoden anderer Klassen.
* Weighted Methods Per Class (WMPC1):
    * die Summe der zyklomatischen Zahlen ZZ aller Methoden der Klasse (ohne geerbte Methoden)
* Number of Remote Methods(NORM):
    * die Anzahl der in einer Klasse gerufenen Methoden "fremder" Klassen.
* Attribute Complexity (AC)
    * die gewichtete Summe der Attribute einer Klasse wird gebildet; Gewichte werden gemäß Typen/Klassen der Attribute vergeben.

# Kapitel 4: Dynamische Programmanalysen und Testen

## Einleitung

#### Fehlerzustand, Fehlerwirkung und Fehlhandlung

* Fehlerzustand (fault) - direkt erkennbar durch statische Tests
    * inkorrektes Teilprogramm, Anweisung, Definition
* Fehlerwirkung (failure) - direkt erkennbar durch dynamische Tests
    * Wirkung eines Fehlerzustandes, die bei der Ausführung des Testobjektes nach "außen" in Erscheinung tritt
    * Abweichung zwischen speizifiziertem Soll-Wert und beobachtetem Ist-Wert
* Fehlhandlung (error)
    * menschliche Handlung, die zu einem Fehlerzustand in der Software führt (vom Entwickler und nicht vom Anwender)
