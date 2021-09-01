# BwInf Template für die ersten beiden Runden

Template für die Bearbeitung der ersten beiden Runden des [Bundeswettbewerbs Informatik (BwInf)](https://bwinf.de/bundeswettbewerb)

## Inhalt

- `/A0_XXX/`: Beispieldaten für eine Aufgabe
- `/A0_XXX/bin`: Ordner für kompilierte Dateien (bei Scriptsprachen leer lassen)
- `/A0_XXX/src`: Ordner für Quelltext
- `/A0_XXX/testinput`: Ordner für Testeingaben
- `/A0_XXX/testoutput`: Ordner für Testausgaben
- `/A0_XXX/compile`: Script zum Kompilieren des Programms für die Aufgabe
- `/A0_XXX/DOC.md`: Dokumentation im Markdown-Format ([Version von pandoc](https://pandoc.org/MANUAL.html#pandocs-markdown))
- `/A0_XXX/run`: Script zum Ausführen (benötigt für automatisches Testen)
- `/output/`: Ordner für ZIP-Inhalt
- `/scripts/`: Bashscripte zur Automatisierung
- `/scripts/clean`: leert `/output`
- `/scripts/copyprog`: kompiliert eine Aufgabe (Parameter) und kopiert sie in `/output`
- `/scripts/download_testcases`: interaktives Script zum Herunterladen aller Testeingaben vom BwInf-Server
- `/scripts/makeall`: ruft die anderen Scripte auf, um die ganze Einsendung zu packen
- `/scripts/makepdf`: ruft pandoc auf, um die PDF-Dokumentation einer Aufgabe (Parameter) zu erstellen
- `/scripts/maketask`: ruft andere Scripte auf, um die Einsendungsdateien einer Aufgabe (Parameter) vorzubereiten
- `/scripts/testtask`: testet das Programm einer Aufgabe mit allen Eingabedateien im Ordner `testinput`
- `/tasknames`: Namen der Aufgaben, die bearbeitet werden
- `/template.tex`: LaTeX-Template, in das die Markdown-Dateien eingebettet werden

# Anpassung

1. alle Aufgabennamen festlegen und in `tasknames` eintragen
1. `A0_XXX` für jede Aufgabe kopieren
1. `/scripts/download_testcases` ausführen
1. `compile` und `run` für jede Aufgabe schreiben
1. Metadaten im Header der Markdowndateien anpassen
1. Dokumentation und Programme ausarbeiten
1. `makeall` ausführen und einsenden

# Abhängigkeiten

- bash
- [pandoc](https://pandoc.org)
- [pandoc-eqnos](https://github.com/tomduck/pandoc-eqnos)
