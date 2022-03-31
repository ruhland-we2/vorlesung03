# Vorlesung03 Projektstruktur und Einführung von SCSS in das Projekt

Das Ergebnis können Sie unter Github Page unter [https://ruhland-we2.github.io/vorlesung03/](https://ruhland-we2.github.io/vorlesung03/) anzeigen lassen.

## Step 1 Aktivieren der Extension in VSC

Um SCSS in Visual Studio Code zu nutzen müssen Sie die Extension **Live Sass Compiler** aktivieren

## Step 2 Globale Variablen

Erstellen Sie eine Datei `_constants.scss` im scripts Verzeichnis. Die Datei sollte nur Globale Variablen beinhalten. der Underscore in scss hat die Bedeutung, dass die Datei nicht in eine css Datei compiliert wird

```scss
$GlobalHeaderBackgroundColor: darkblue;
$GlobalHeaderHeight: 80px;
$GlobalHeaderColor: white;
```