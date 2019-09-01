# Angepasste TonUINO Version

Als Grundlage hier wurden die Dateien aus der originalen 2.1 DEV Vesion genommen und die .ino Datei mit den folgenden zusätzlichen Funktionen erweitert. Der zusätzliche Code wird so in meinen Projekten erfolgreich genutz.

Jede Erweiterung wird am Anfang der .ino Datei mit dem entsprechenden "#define" Text definiert. Sollte diese Zeile als Kommentar markiert werden, so wird die gesamte Funktion beim Upload nicht berücksichtigt und nimmt daher keinen Platz auf dem Arduino ein. Zum aktivieren müssen diese entsprechend entfernt werden.

Für die Funktionen des TonUINO bitte im Originalprojekt nachlesen.

## Kopfhöreranschluss und Lautstärkenbegrenzung im Kopfhörermodus
"#define JACKDETECT" (zum aktivieren auskommentieren)
https://discourse.voss.earth/t/kopfhoererbuchsenplatine/2463/44
- Speichert die aktuelle Lautstärke vor dem Anschließen ab.
- Beim Anschluss des Kopfhörers wird eine bestimmte Lautstärke und eine maximale Lautstärke im Kopfhörermodus aktiviert.
- Beim Ausstecken wird auf die zuvor gespeicherte Lautstärke zurückgesetzt


## LED Strip und Ring
"#define LED_SR" (bereits aktiviert)
https://discourse.voss.earth/t/integration-led-strip-und-ring-mit-neopixel/2760
- Default (Keine Karte erkannt): Wechselnde Füllung aller LED im gesamten Farbspektrum
- Musik spielt: RainbowCycle (nachgebaut)
- Musik pausiert: Aufsteigende Füllung in Regenbogenfarben
- Lautstärkeanpassung: Prozentuale Anzeige (angepasst an eingestellte minimale und maximale Lautstärke) in der Skala grün zu gelb zu rot
- Nächstes Lied: Aufsteigende Füllung in Grün (kann ganz am Anfang über Variable als RGB schnell geändert werden)
- Lied zurück: Absteigende Füllung in Blau (kann ganz am Anfang über Variable als RGB schnell geändert werden)

## Ein und Ausschalen der LEDs über die Knöpfe
"#define LED_SR_Switch" (zum aktivieren auskommentieren)
- Einschalten über gemeinsames langes drücken von Lauter und Pause Knopf
- Ausschalten über gemeinsames langes drücken von Leise und Pause Knopf

## Ein und Ausschalen der LEDs über die Knöpfe
"#define LED_SR_Powersafe" (bisher noch kein Code enthalten)

