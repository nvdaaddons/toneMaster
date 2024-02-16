# Tone-Master #

* Authors: Hrvoje Katić
* [Stabile Version herunterladen][1]
* NVDA-Kompatibilität: 2019.3 und neuer

Willkommen beim Tone-Master! Diese NVDA-Erweiterung habe ich eigentlich nur
aus Spaß erstellt. vielleicht finden Sie auch Gefallen daran.

Ich wollte schon immer mal musikalische Klänge mit NVDA erzeugen, lieber als
nur die Signaltöne von Fortschrittsbalken oder akustischen Signale bei
Fehlern in NVDA zu hören. Allerdings ist das ganz und gar nicht so
leicht. Ich wollte es einfacher machen. Deshalb habe ich den Tone-Master
geschrieben. Allein schon die witzige Vorstellung wie das sein könnte, wenn
NVDA Musikstücke von Mozart, Beethoven oder auch die größten Hits von den
Rolling Stones abspielt. Dabei hören sich die Klänge wie die Klingeltöne von
alten Mobiltelefonen an. Das dürfte auch heute noch sehr witzig sein.

Der Tone-Master vereinfacht die Wiedergabe von Tonfolgen durch
Klang-Dateien. Diese können Sie mit einem gewöhnlichen Editor Ihrer Wahl
bearbeiten, um sie anschließend in NVDA abspielen zu können!

## Klang-Dateien

Bevor Sie Ihre ersten musikalischen Klänge mit Tone-Master abspielen können,
müssen Sie erst eine Klang-Datei erstellen und diese laden. Die
Klang-Dateien sind einfache Textdateien, nur mit der Endung ".tdf". Der Tone
Master verarbeitet und spielt die Tonfolgen ab. Nachstehend werden ein paar
Regeln kurz erklärt, damit solche Dateien überhaupt abgespielt werden
können.

1. Jede Zeile in der Klang-Datei enthält drei Werte, die jeweils mit einem
   Doppelpunkt von einander getrennt werden. Der erste Wert gibt die Tonhöhe
   an, der zweite Wert die Länge und der dritte Wert die Stille am
   Ende. Dabei sind stets alle drei Parameter notwendig, sonst könn die
   Dateien im Tone-Master nicht abgespielt werden.
2. Die Angaben zur Tonhöhe und Länge müssen aus positiven Werten bestehen,
   wobei die Länge in Kommazahlen angegeben werden. Dabei ist noch zu
   beachten, dass hierbei nicht das deutsche Komma verwendet werden darf,
   sondern der Punkt.
3. Das Nummernzeichen am Anfang einer Zeile wird vom Tone-Master als
   Kommentar betrachtet und somit ignoriert.

Beispiel: Wiedergabe einer Tonfolge bestehend aus drei Tönen

1500:100:0.5

1000:100:0.09

500:100:0.7

In diesem Beispiel hat der erste Ton eine Tonhöhe von 1500 Hertz, eine Länge
von 100 Millisekunden und 0.5 Millisekunden Stille. Die zweite Tonhöhe von
1000 Hertz und eine Länge von 100 Millisekunden und 0.09 Millisekunden
Stille. Der letzte Ton hat eine Tonhöhe von 500 Hertz, eine Länge von 100
Millisekunden und 0.7 Millisekunden Stille.

Hinweis: Der Parameter für die Stille ist besonders wichtig, ansonsten
überlagert NVDA  den vorherigen mit dem nächsten Ton, wobei das dann zu
unerwünschten Effekten führen kann.

Um sich vertrauter mit der ganzen Syntax zu machen, können Sie sich
natürlich an der Beispieldatei in dieser NVDA-Erweiterung orientieren. Diese
befindet sich im Ordner "Tones", wo üblicherweise sich die Klang-Dateien
ebenso befinden sollten.

## Kurztastenbefehle

* Alt+NVDA+T: Spielt die aktuelle Klang-Datei ab.
* Alt+Umschalt+NVDA+T: Unterbricht die momentan abzuspielende Klang-Datei.
* Alt+NVDA+N: Erstellt und öffnet eine neue Klang-Datei im Editor.
* Alt+NVDA+L: Zeigt ein Dialogfeld zum Wiedergeben an, indem Sie eine
  bereits geladene Klang-Datei erneut auswählen können.
* Alt+NVDA+E: Öffnet die aktuell geladene Klang-Datei im Editor.
* Alt+NVDA+O: Öffnet einen Ordner, indem Sie die entsprechende Klang-Datei
  auswählen und laden können.

## Weitere Anmerkungen

Sie können entweder Klang-Dateien erstellen, bearbeiten und laden oder zu
den Ordnern wechseln, die schon erstellte Dateien beinhalten. Sie gelangen
zu den Ordnern über das NVDA-Menü > Werkzeuge > Tone-Master.

Wenn das Dialogfeld zum Erstellen von neuen Klang-Dateien angezeigt wird,
können Sie den Namen (ohne die Endung ".tdf") direkt eingeben. Die Endung
wird automatisch vom Tone-Master angehängt. Falls kein Name angegeben wurde,
wird standardmäßig "Untitled.tdf" genommen. Der Tone-Master erstellt
anschließend eine neue Datei und öffnet sie im Editor. Mit der Escape-Taste
können Sie den Vorgang abbrechen.

Hinweis: Der Tone-Master verwendet standardmäßig zum Bearbeiten der
Klang-Dateien den Windows-Editor.

Wenn das Dialogfeld zum Öffnen von Klang-Dateien angezeigt wird, können Sie
mit den Pfeiltasten eine Datei auswählen und sie mit der Eingabetaste öffnen
oder den Dialog mit der Escape-Taste abbrechen.

Wenn Sie einen Ordner mit einer .tdf-Datei öffnen, können Sie die Datei zum
Anzeigen und Bearbeiten im Editor laden. Um sich die Ergebnisse sofort
anhören zu können, wird empfohlen die Datei im Tone-Master erst zu
laden. Anshließend können Sie die Datei bearbeiten, speichern und danach das
Ergebnis nochmal abspielen.

## Änderungen in 1.3

* Es wurde ein Kompatibilitätsproblem mit neueren NVDA-Versionen behoben.

## Änderungen in 1.2

* Behoben: Ein Problem, bei dem man erst eine leere Klang-Datei laden
  konnte, anschließend eine andere öffnete und eine Fehlermeldung, dass
  keine abgespielt wurde, auftrat.

## Änderungen in 1.1

* Hinzugefügt: Eine Option zum Erstellen und Bearbeiten von neuen
  Klang-Dateien im Editor.
* Hinzugefügt: Eine Option zum Bearbeiten von bereits geladenen
  Klang-Dateien im Editor.
* Verbessert: Fehlermeldungen sind nun aussagekräftiger.
* Verbessert: Unter Umständen werden bestimmte Features der NVDA-Erweiterung
  beispielsweise das Öffnen oder Bearbeiten von Klang-Dateien im Editor nun
  in geschützten Desktop aus Sicherheitsgründen unterbunten.
* Verbessert: NVDA teilt nun mit, wenn eine Wiedergabe unterbrochen wird.
* Behoben: Solange eine Klang-Datei wiedergegeben wird, llässt sich keine
  weitere laden.

## Änderungen in 1.0

* Erste Version.

[[!tag stable]]

[1]: https://addons.nvda-project.org/files/get.php?file=tmast
