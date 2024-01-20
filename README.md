# Chip-8 Emulator

Dieses Projekt ist ein Emulator für den Chip-8, der in C# geschrieben ist. Der Chip-8 ist ein einfacher, interpretierter, portabler Computer, der in den 1970er Jahren entwickelt wurde.

## Struktur des Projekts

Das Projekt besteht aus zwei Hauptklassen: `CPU` und `Program`.

### CPU

Die `CPU`-Klasse implementiert die Logik des Chip-8. Sie enthält den Speicher, die Register und den Stack des Chip-8. Außerdem implementiert sie die Methoden zum Laden von Programmen und zum Ausführen von Befehlen.

### Program

Die `Program`-Klasse ist der Einstiegspunkt des Emulators. Sie initialisiert die CPU, lädt das zu emulierende Programm und startet die Hauptschleife, die die CPU anweist, Befehle auszuführen und den Bildschirm zu aktualisieren.

## Verwendung

Um den Emulator zu verwenden, müssen Sie ein Chip-8-Spiel in Form einer Binärdatei haben. Diese Datei wird dann an die `LoadProgram`-Methode der `CPU`-Klasse übergeben. Anschließend können Sie die `Step`-Methode der `CPU`-Klasse in einer Schleife aufrufen, um das Programm auszuführen.

## Tastatureingaben

Die Tastatureingaben werden durch die `KeyPressed`-Methode der `CPU`-Klasse verarbeitet. Wenn eine Taste gedrückt wird, wird der entsprechende Opcode in das Register geladen, und der Programmzähler wird um zwei erhöht.

## Grafikausgabe

Die Grafikausgabe wird durch die SDL2-Bibliothek gehandhabt. Die Pixel des Bildschirms werden in einem Array gespeichert und dann auf den Bildschirm gezeichnet.

## Audioausgabe

Die Audioausgabe wird ebenfalls durch die SDL2-Bibliothek gehandhabt. Ein einfacher Sinuston wird erzeugt, wenn der Sound-Timer des Chip-8 größer als null ist.

## Build

Um das Projekt zu bauen, öffnen Sie die `chip-8.sln` Datei in Visual Studio und drücken Sie `Ctrl+Shift+B`, oder wählen Sie `Build Solution` aus dem `Build`-Menü.

## Lizenz

Dieses Projekt ist unter der MIT-Lizenz lizenziert. Siehe die `LICENSE`-Datei für Details.
