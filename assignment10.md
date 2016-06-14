# Test-driven Development (TDD)

## Grundidee

*  Schreibe NIEMALS Business Code, außer ein Testfall schlägt fehl.
*  Eliminiere alle Duplikate, die du findest.

## Vorgehen
![Imgur](http://i.imgur.com/LuZMrH8.png?1)

1. „Überlege“ wünschenswertes Verhalten,
das im Moment nicht vorhanden  ist.\s\s
2. Schreibe einen Testfall der dieses
Verhalten erzeugt (und somit auch
fehlschlägt).\s\s
3. Schreibe Code der den Testfall nicht
mehr fehlschlagen lässt.\s\s
4. Verbessere  den Code  durch Refactoring.\s\s

## Pro
* "freie" Unittests und komplette Test-Suite entsteht bei der Entwicklung mit TDD
* fördert Codeverständnis ("Wie würde man dieses Feature implementieren und dann Testen?")
* Code muss modular werden (sonst kaum Test möglich)
* einfachere Dokumentation
* Fehler werden schnell erkannt

## Con
* erfordert hohen Aufwand beim Maintaining der Test-Suite
* 1 Projekt wird zu 2 Projekten (Tests + eigtl. Anwendung)
* bei komplexen Projekten sind sehr komplexe Tests nötig
* kein schnelles Development --> kaum Anpassungsfähigkeit an wandelnde Requirements

## Eigene Meinung
* bei derzeitigen Projekten nicht sinnvoll
* Potential von TDD erkennbar
* Implementation der Test-Suite zu aufwendig
