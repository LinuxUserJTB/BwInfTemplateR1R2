# BwInf Template für die ersten beiden Runden

Template für die Bearbeitung der ersten beiden Runden des [Bundeswettbewerbs Informatik (BwInf)](https://bwinf.de/bundeswettbewerb)

## Inhalt

- `/demo/`: Beispieldaten für eine Aufgabe
- `/demo/bin`: Ordner für kompilierte Dateien (bei Scriptsprachen leer lassen)
- `/demo/src`: Ordner für Quelltext
- `/demo/testinput`: Ordner für Testeingaben
- `/demo/testoutput`: Ordner für Testausgaben
- `/demo/compile`: Script zum Kompilieren des Programms für die Aufgabe
- `/demo/DOC.md`: Dokumentation im Markdown-Format ([Version von pandoc](https://pandoc.org/MANUAL.html#pandocs-markdown))
- `/demo/run`: Script zum Ausführen (benötigt für automatisches Testen)
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
- `/templateR1.tex`: LaTeX-Template, in das die Markdown-Dateien eingebettet werden (Runde 1)
- `/templateR2.tex`: LaTeX-Template, in das die Markdown-Dateien eingebettet werden (Runde 2)

## Anpassung / Benutzung

1. für die erste Runde: keine Vorbereitung der Dateien nötig
1. für die zweite Runde
	- `/scripts/makepdf` bearbeiten und in der dritten Zeile `templateR1.tex` durch `templateR2.tex` ersetzen
	- Inhalt von `/A0_XXX/DOCR2.md` in `/A0_XXX/DOC.md` kopieren
1. `/A0_XXX/DOCR2.md` wird nun nicht mehr gebraucht
1. alle Aufgabennamen festlegen und in `tasknames` eintragen
1. `/scripts/setup` ausführen
1. die Ordner `/demo/` und `A0_XXX` werden nun nicht mehr gebraucht
1. `/scripts/download_testcases` ausführen
	- Beispiel für die Eingabe: https://bwinf.de/fileadmin/user_upload/parkplatz0.txt (bis parkplatz5.txt)
	- `https://bwinf.de/fileadmin/user_upload` ist der Basis-URL
	- `parkplatz` ist der Code-Name
	- `0` ist der erste Testfall, `5` der letzte
1. `/Ax_???/compile` und `/A?_???/run` für jede Aufgabe schreiben
1. Metadaten im Header der Markdowndateien anpassen
1. Dokumentation und Programme ausarbeiten
1. `makeall` ausführen und einsenden

## Abhängigkeiten

- bash
- [pandoc](https://pandoc.org)
- [pandoc-eqnos](https://github.com/tomduck/pandoc-eqnos)
