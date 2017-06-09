# Tone Master #

* Autor: Hrvoje Katić
* Herunterladen der [stabilen Version][1]

Willkommen beim Tone Master! Diese NVDA-Erweiterung habe ich eigentlich nur
zum Vergnügen erstellt, aber hoffe auch, dass Sie bei der Verwendung Freude
dabei haben werden.

Ich wollte schon immer mal musikalische Töne mit NVDA erzeugen, lieber als
nur die Signaltöne von Fortschrittsbalken oder akustischen Signale bei
Fehlern in NVDA hören. Allerdings ist das ganz und gar nicht so leicht. So
wollte ich es erst einfacher machen. Das ist, warum ich den Tone Master
geschrieben habe. Alleine die Vorstellung, wie das sein könnte, wenn NVDA
Musikstücke von Mozart, Beethoven oder auch die größten Hits von den Rolling
Stones spielen könnte. Dabei hören sich die Klänge wie die Klingeltöne von
alten Mobiltelefonen an. Das dürfte auch weiterhin sehr witzig sein.

Tone Master vereinfacht die Wiedergabe von Tonfolgen durch
Klangdateien. Diese Dateien können Sie mit einem gewöhnlichen Editor Ihrer
Wahl bearbeiten, um sie anschließend in NVDA abspielen lassen zu können.

## Klangdateien

Bevor Sie Ihre ersten musikalischen Töne mit Tone Master abspielen können,
müssen Sie erst eine Klangdatei erstellen und diese laden. Die Klangdateien
sind einfache Textdateien, nur mit der Endung ".tdf". Der Tone Master
verarbeitet und spielt die Tonfolgen ab. Nachstehend werden ein paar Regeln
kurz erklärt, damit solche Dateien überhaupt abspielen zu können.

1. Jede Zeile in der Klangdatei enthält drei Werte, die jeweils mit einem
   Doppelpunkt von einander getrennt werden. Der erste Wert gibt die Tonhöhe
   an, der zweite Wert die Länge und der dritte Wert die Stille am
   Ende. Dabei sind stets alle drei Parameter notwendig, sonst kann der Tone
   Master die Datei nicht abspielen.
2. Die Angaben zur Tonhöhe und Länge müssen aus positiven Werten bestehen,
   wobei die Länge in Kommazahlen angegeben werden. Dabei ist noch zu
   beachten, dass hierbei nicht das deutsche Komma verwendet werden darf,
   sondern der Punkt.
3. Mit dem Nummernzeichen am Anfang einer Zeile wird diese vom Tone Master
   ignoriert.

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
natürlich an der Beispieldatei in dieser NVDA-Erweiterung, die sich im
Ordner "Tones" befindet, wo üblicherweise sich die Klangdateien ebenso
befindenden sollten, orientieren.

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

## Anmerkungen

Sie können auch die Klangdateien erstellen, bearbeiten und laden oder
wechseln Sie in den Ordner über das NVDA-Menü "Extras" > "Tone Master",
indem sich die Dateien befinden.

Wenn das Dialogfeld zum Erstellen von neuen Klangdateien angezeigt wird,
können Sie den Namen (ohne die Endung ".tdf") direkt eingeben. Die Endung
wird automatisch vom Tone Master angehängt. Falls kein Name angegeben wurde,
wird standardmäßig "Untitled.tdf" genommen. Tone Master erstellt
anschließend eine neue Datei und öffnet sie im Editor. Mit der Escape-Taste
können Sie den Vorgang abbrechen.

Hinweis: Der Tone Master verwendet standardmäßig zum Bearbeiten der
Klangdateien den Windows-Editor.

Wenn das Dialogfeld zum Öffnen von Klangdateien angezeigt wird, können Sie
sich mit den Pfeiltasten eine Klangdatei auswählen und sie mit der
Eingabetaste schließlich öffnen oder mit der Escape-Taste abbrechen.

Wenn Sie einen Ordner mit einer .tdf-Datei öffnen, können Sie sie zum
Anzeigen und Bearbeiten im Editor laden. Um die Ergebnisse sofort sich
anhören zu können, wird empfohlen, die Datei im Tone Master erst zu
laden. Anshließend können Sie die Datei bearbeiten, speichern und danach das
Ergebnis sich nochmal anhören.

## Änderungen in Version 1.2

* Behoben: Ein Problem, in dem man erst eine leere Datei laden konnte,
  anschließend eine andere öffnete, und diese versuchte wiederzugeben,
  endete mit der Meldung, dass keine Datei abgespielt wurde.

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
* Behoben: Solange eine Datei bereits wiedergegeben wird, kann man keine
  weitere laden.

## Änderungen in Version 1.0

* Erste Veröffentlichung.

[[!tag dev stable]]

[1]: https://addons.nvda-project.org/files/get.php?file=tmast
