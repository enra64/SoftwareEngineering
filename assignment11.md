## TASK 1
### Fehlerkategorien

#### Compilerfehler
Fehler in der Sprache, die den Compiler daran
hindern, dass Programm zu übersetzen

##### Behebung
* Compiler Errors vor Ausführung des Codes bemerkbar
* Lassen sich (meist) auf eine präzise Codezeile zurückverfolgen
* meistens durch IDE visualisiert

##### Beispiele
  * Typos
  * Klammersetzung
  * Typsystemfehler

#### Laufzeitfehler
Fehler, die während der Ausführung des Codes auftreten.
Laufzeitfehler werden in der Regel automatisch erkannt.

##### Behebung
* Bei Auftreten des Problems kommt i.d.R eine Exception
* Stacktrace der Exception gibt Aufschluss über den Context (Call-Reihenfolge)
* Stacktrace verweist auf entsprechende Codezeile
* Verstehen, warum an dieser Stelle der Fehler aufgetreten ist, ist schwieriger -> Schrittweises Debuggen

##### Beispiele
  * Value out of Range
  * Division by Zero
  * Null Pointer References


#### Logische Fehler
Fehler, bei denen sich das Programm nicht wie
erwartet verhält. Kein Fehler im Code, sondern im Verständnis des Programmierers.

##### Behebung
* Fehler entsteht, weil das Codeverständnis bei der
Programmierung nicht ausreichte
* Debug-Methoden helfen dabei, Codeverständnis aufzubauen
* Abhängig von Symptom und Komplexität des Codes kommen verschiedenste Debugging-Methoden zum Einsatz
* Am Ende jedoch muss der Entwickler verstehen, warum er einen Fehler gemacht hat

##### Beispiele
  * Falsches Ergebnis
  * Falsches Ergebnis
  
  
## TASK 2
### Version Control System
#### Definition

##### Zentrale VCS
* Zentrale Kopie des gesamten Projekts auf Server
* durch Rechteverwaltung wird dafür gesorgt, dass nur berechtigte Personen neue Versionen in das Archiv legen können
* Versionsgeschichte ist hierbei nur im Repository vorhanden
* benötigte Dateien werden auds dem zentralen Repo geladen

##### Pros
* benötigt wenig lokalen Speicher
* nur ein Repository muss beachtet werden, das zentrale

##### Cons
* gesamtes Projekt nur auf dem Server
* Änderungskonflikte müssen manuell aussortiert werden
* keine lokalen Historien

##### Beispiele
* SVN, CVS

---
#### Dezentrale VCS
* dezentrale (lokale) Kopien des gesamten Projekts
* Jeder, der an dem verwalteten Projekt arbeitet, hat sein eigenes (lokales) Repository und arbeitet an diesem
* Versionsgeschichte ist dadurch auf Repos verteilt
* Änderungen können lokal verfolgt werden
* kein Konflikt, wenn mehrere Benutzer dieselbe Version einer Datei ändern, denn widersprechenden Versionen existieren zunächst parallel und können weiter geändert und gemerged werden

##### Pros
* Änderungen sind sehr schnell möglich aufgrund des lokalen Repos  _ Ausnahme: pushing und pulling zum Server _
* Commits können gesammelt werden und dann gesammelt in das Netwerkrepo gepusht werden
* arbeiten am Projekt komplett offline möglich  
_ Ausnahme: pushing und pulling zum Server _
* da jeder Programmierer über das komplette Projekt verfügt können einzelne Commits an einzelne Programmierer zur Überprufung weitergegeben werden (Verhindert Fehler bei offenen Repos)

##### Cons
* Server braucht viel Speicher bei sich oft ändernden großen Binärdateien (komplette History gespeichert)
* Herunterladen der gesamten Historie benötigt bei großen Projekten viel Zeit und Speicherplatz

##### Beispiele
* Git, Mercurial

---
### Persönlicher Favorit
* ** GIT **
* ##### Gründe
  * Git ist sehr gut, sehr schnell, sehr geil
  * GitHub
  * OpenSource
  * 
 

## TASK 5

### Softwaremetriken

#### Beispiele

__*Größenmetriken*__
* Bsp.: Lines of Code

__*Strukturmetriken*__
* Bsp.: Eigenschaften des Kontrollflussgraphen

__*Komplexitätsmetriken*__
* Bsp.: McCabe Cyclomatic Complexity


#### Metrik-Berechnung wie und am Beispiel zeigen

__*Größenmetriken*__
* Lines of Code(LOC) zählt die (ausführbaren) Codezeilen eines Programms
* Kommentare etc. werden nicht mit hinein gezählt
* Berechnung am Beispiel: Siehe Übung 10.3 => Lines of Code = 12

__*Strukturmetriken*__
* Zählt die Knoten, Kanten oder die Tiefe des Kontrollflussgraphen
* Berechnung am Beispiel: Siehe Übung 10.3 =>
 * #Knoten = 11
 * #Kanten = 14
 * Min. Tiefe = 5
 * Max. Tiefe = 7

__*Komplexitätsmetriken*__
* McCabe basiert auf Kontrollflussgraph
*  C = #Kanten - #Knoten + 2 * #Funktionen
* Berechnung am Beispiel: Siehe Übung 10.3 a) => C = 14 - 11 + 2*1 = 5


#### Vor- bzw. Nachteile

__*Größenmetriken (LOC)*__
* Vorteile:
 * relativ einfach messbar
 * starke Korrelation mit anderen Maßen

* Nachteile:
 * ignoriert Komplexität von Anweisungen und Strukturen
 * schlecht vergleichbar

__*Strukturmetriken (Eigenschaften Graph)*__
* Vorteile:
 * einfach messbar
 * Ausgangspunkt für andere Metriken (z.B. McCabe)
* Nachteile:
 * Ablauf-Komplexität wird nicht gemessen
 * gut vergleichbar 

__*Komplexitätsmetriken (McCabe)*__
* Vorteile:
 * einfach zu berechnen
 * Ablauf-Komplexität wird gemessen
* Nachteile:
 * Modulkomplexität wird nicht berücksichtigt
