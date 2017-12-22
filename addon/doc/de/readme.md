# Tone Master #

* Autor: Hrvoje Katić
* Herunterladen der [stabilen Version][1]

Willkommen beim Tone Master! Diese NVDA-Erweiterung habe ich eigentlich nur
aus Spaß erstellt. Ich hoffe, dass Sie bei der Verwendung auch Gefallen an
dieser Erweiterung finden.

Ich wollte schon immer mal musikalische Töne mit NVDA erzeugen, lieber als
nur die Signaltöne von Fortschrittsbalken oder akustischen Signale bei
Fehlern in NVDA zu hören. Allerdings ist das ganz und gar nicht so
leicht. Ich wollte es einfacher machen. Deshalb habe ich den Tone Master
geschrieben. Allein schon die witzige Vorstellung wie das sein könnte, wenn
NVDA Musikstücke von Mozart, Beethoven oder auch die größten Hits von den
Rolling Stones abspielt. Dabei hören sich die Klänge wie die Klingeltöne von
alten Mobiltelefonen an. Das dürfte auch heute noch sehr witzig sein.

Tone Master vereinfacht die Wiedergabe von Tonfolgen durch
Klangdateien. Diese Dateien können Sie mit einem gewöhnlichen Editor Ihrer
Wahl bearbeiten, um sie anschließend in NVDA abspielen zu können.

## Klangdateien

Bevor Sie Ihre ersten musikalischen Töne mit Tone Master abspielen können,
müssen Sie erst eine Klangdatei erstellen und diese laden. Die Klangdateien
sind einfache Textdateien, nur mit der Endung ".tdf". Der Tone Master
verarbeitet und spielt die Tonfolgen ab. Nachstehend werden ein paar Regeln
kurz erklärt, damit solche Dateien überhaupt abgespielt werden können.

1. Jede Zeile in der Klangdatei enthält drei Werte, die jeweils mit einem
   Doppelpunkt von einander getrennt werden. Der erste Wert gibt die Tonhöhe
   an, der zweite Wert die Länge und der dritte Wert die Stille am
   Ende. Dabei sind stets alle drei Parameter notwendig, sonst kann der Tone
   Master die Datei nicht abspielen.
2. Die Angaben zur Tonhöhe und Länge müssen aus positiven Werten bestehen,
   wobei die Länge in Kommazahlen angegeben werden. Dabei ist noch zu
   beachten, dass hierbei nicht das deutsche Komma verwendet werden darf,
   sondern der Punkt.
3. Das Nummernzeichen am Anfang einer Zeile wird vom Tone Master als
   Kommentar betrachtet und somit ignoriert.

Beispiel: Wiedergabe einer Tonfolge bestehend aus drei Tönen.

1500:100:0.5

1000:100:0.09

500:100:0.7

In diesem Beispiel hat der erste Ton eine Tonhöhe von 1500 Hz, eine Länge
von 100 ms und 0.5 ms Stille. Die zweite Tonhöhe von 1000 Hz und eine Länge
von 100 ms und 0.09 ms Stille. Der letzte Ton hat eine Tonhöhe von 500 Hz,
eine Länge von 100 ms und 0.7 ms Stille.

Hinweis: Der Parameter für die Stille ist besonders wichtig, ansonsten
überlagert NVDA  den vorherigen mit dem nächsten Ton, wobei das dann zu
unerwünschten Effekten führen kann.

Um sich vertrauter mit der ganzen Syntax zu machen, können Sie sich
natürlich an der Beispieldatei in dieser NVDA-Erweiterung orientieren. Diese
befindet sich im Ordner "Tones", wo üblicherweise sich die Klangdateien
ebenso befinden sollten.

## Kurztastenbefehle

* Alt+NVDA+T: Spielt die aktuelle Klangdatei ab.
* Alt+Shift+NVDA+T: Sofern bereits eine Klangdatei wiedergegeben wird, wird
  damit die aktuelle Wiedergabe angehalten.
* Alt+NVDA+N: Erstellt und öffnet eine neue, leere Klangdatei zum Bearbeiten
  im Editor.
* Alt+NVDA+L: Zeigt ein Dialogfeld zum Wiedergeben an, indem Sie eine
  bereits geladene Datei erneut auswählen können.
* Alt+NVDA+E: Öffnet die aktuell geladene Klangdatei zum Bearbeiten im
  Editor.
* Alt+NVDA+O: Öffnet einen Ordner, indem Sie die entsprechende Klangdatei
  auswählen und laden können.

## Weitere Anmerkungen

Sie können entweder Klangdateien erstellen, bearbeiten und laden oder zu den
Ordnern wechseln, die schon erstellte Dateien beinhalten. Sie gelangen zu
den Ordnern über das NVDA-Menü "Extras" > "Tone Master".

Wenn das Dialogfeld zum Erstellen von neuen Klangdateien angezeigt wird,
können Sie den Namen (ohne die Endung ".tdf") direkt eingeben. Die Endung
wird automatisch vom Tone Master angehängt. Falls kein Name angegeben wurde,
wird standardmäßig "Untitled.tdf" genommen. Tone Master erstellt
anschließend eine neue Datei und öffnet sie im Editor. Mit der Escape-Taste
können Sie den Vorgang abbrechen.

Hinweis: Der Tone Master verwendet standardmäßig zum Bearbeiten der
Klangdateien den Windows-Editor.

Wenn das Dialogfeld zum Öffnen von Klangdateien angezeigt wird, können Sie
mit den Pfeiltasten eine Klangdatei auswählen und sie mit der Eingabetaste
öffnen oder den Dialog mit der Escape-Taste abbrechen.

Wenn Sie einen Ordner mit einer .tdf-Datei öffnen, können Sie die Datei zum
Anzeigen und Bearbeiten im Editor laden. Um sich die Ergebnisse sofort
anhören zu können, wird empfohlen die Datei im Tone Master erst zu
laden. Anshließend können Sie die Datei bearbeiten, speichern und danach das
Ergebnis nochmal abspielen.

## Änderungen in Version 1.2

* Behoben: Ein Problem, bei dem man erst eine leere Datei laden konnte,
  anschließend eine andere öffnete und eine Fehlermeldung, dass keine Datei
  abgespielt wurde, auftrat.

## Änderungen in Version 1.1

* Hinzugefügt: Eine Option zum Erstellen und Bearbeiten von neuen
  Klangdateien im Editor.
* Hinzugefügt: Eine Option zum Bearbeiten von bereits geladenen Klangdateien
  im Editor.
* Verbessert: Fehlermeldungen sind nun aussagekräftiger.
* Verbessert: Unter Umständen werden bestimmte Features der Erweiterung
  beispielsweise das Öffnen oder Bearbeiten von Klangdateien im Editor nun
  im geschüttzen Desktop untersagt.
* Verbessert: NVDA teilt nun mit, wenn eine Wiedergabe angehalten wird.
* Behoben: Solange eine Datei wiedergegeben wird, kann man keine weitere
  laden.

## Änderungen in Version 1.0

* Erste Veröffentlichung.

[[!tag dev stable]]

[1]: https://addons.nvda-project.org/files/get.php?file=tmast
