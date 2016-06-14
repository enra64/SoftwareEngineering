## Task 1
#### Test-driven Development (TDD)

#### Grundidee

*  Schreibe NIEMALS Business Code, außer ein Testfall schlägt fehl.
*  Eliminiere alle Duplikate, die du findest.

#### Vorgehen
![Imgur](http://i.imgur.com/LuZMrH8.png?1)

1. „Überlege“ wünschenswertes Verhalten,
das im Moment nicht vorhanden  ist.\s\s
2. Schreibe einen Testfall der dieses
Verhalten erzeugt (und somit auch
fehlschlägt).\s\s
3. Schreibe Code der den Testfall nicht
mehr fehlschlagen lässt.\s\s
4. Verbessere  den Code  durch Refactoring.\s\s

#### Pro
* "freie" Unittests und komplette Test-Suite entsteht bei der Entwicklung mit TDD
* fördert Codeverständnis ("Wie würde man dieses Feature implementieren und dann Testen?")
* Code muss modular werden (sonst kaum Test möglich)
* einfachere Dokumentation
* Fehler werden schnell erkannt

#### Con
* erfordert hohen Aufwand beim Maintaining der Test-Suite
* 1 Projekt wird zu 2 Projekten (Tests + eigtl. Anwendung)
* bei komplexen Projekten sind sehr komplexe Tests nötig
* kein schnelles Development --> kaum Anpassungsfähigkeit an wandelnde Requirements

#### Eigene Meinung
* bei derzeitigen Projekten nicht sinnvoll
* Potential von TDD erkennbar
* Implementation der Test-Suite zu aufwendig

## Task 2

Black-Box-Test bezeichnet eine Methode des Softwaretests, bei der die Tests ohne Kenntnisse über die innere Funktionsweise des zu testenden Systems entwickelt werden. 
Er beschränkt sich auf funktionsorientiertes Testen, d. h. für die Ermittlung der Testfälle werden nur die Anforderungen, aber nicht die Implementierung des Testobjekts herangezogen. 
Die genaue Beschaffenheit des Programms wird nicht betrachtet, sondern vielmehr als Black Box behandelt. Nur nach außen sichtbares Verhalten fließt in den Test ein.

Der Begriff White-Box-Test bezeichnet eine Methode des Software-Tests, bei der die Tests mit Kenntnissen über die innere Funktionsweise des zu testenden Systems entwickelt werden. 
Im Gegensatz zum Black-Box-Test ist für diesen Test also ein Blick in den Quellcode gestattet, d. h. es wird am Code geprüft.


* White-Box für Lokalisierung von Fehlern in Teilkomponenten

* Black-Box für Fehlerfindung gegenüber der Spezifikation

---
* Beispiel: PKeS
 * Black-Box - macht der Bot was er soll? (einzelne Fehler kompensieren sich)
 * White-Box - ob einzelne Teilfunktionen funktionieren
 

 
## Task 3
 
![Imgur](http://i.imgur.com/pxRaMgG.png)

#### a) Zyklomatische Komplexität (sollte nie größer als 10 sein)

C = #Kanten - #Nodes + 2*#Funktionen

C = 14 - 11 + 2*0

C = 3 

#### b) Testfälle für die Statement Coverage
„Jedes Statement/Knoten wurde einmal besucht.“

100%ige Überdeckung durch:
T1(-10,-15)

#### c) Testfälle für die Decision Coverage
„Jeder Zweig/Kante wurde einmal besucht.“

100%ige Überdeckung durch:
T1(-10,-15), T2(10,15)


