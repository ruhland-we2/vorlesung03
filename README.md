# Vorlesung03 Projektstruktur und Einführung von SCSS in das Projekt

Das Ergebnis können Sie unter Github Page unter [https://ruhland-we2.github.io/vorlesung03/](https://ruhland-we2.github.io/vorlesung03/) anzeigen lassen.

## Step 1 Aktivieren der Extension in VSC

Um SCSS in Visual Studio Code zu nutzen müssen Sie die Extension **Live Sass Compiler** aktivieren

## Step 2 Globale Variablen und _constants.scss

Erstellen Sie eine Datei `_constants.scss` im scripts Verzeichnis. Die Datei sollte nur Globale Variablen beinhalten. der Underscore in scss hat die Bedeutung, dass die Datei nicht in eine css Datei compiliert wird

```scss
$GlobalHeaderBackgroundColor: darkblue;
$GlobalHeaderHeight: 80px;
$GlobalHeaderColor: white;
```

## Step 3 Erstellen der page-map.scss

Einbinden der Globalen Variablen und Definition in einem hierarchischen Baum
```scss
@import "../_constants";

#page-map{
    background-color: lightblue;

    &-header{
        position: absolute;
        left: 0;
        right: 0;
        top: 0;
        height: $GlobalHeaderHeight;
        color: $GlobalHeaderColor;
        background-color: $GlobalHeaderBackgroundColor;
    }
...
```

Der Live Sass Compiler erstellt dann automatisch die page-map.css sowie eine map-Datei page-map.css.map. Diese bewirkt, dass der Browser im Inspektor die Zeilen der scss Datei anzeigt.

## Step 4 Vendor Prefixes

Vendor Prefixes sind etwas gemeines, das sind Browser spezifische Einstellungen in CSS. Z.B. gibt es diese bei `display: flex;` in CSS. SCSS löst dieses Problem beim compilieren.
Das Ergebnis ist dann in der css-Datei

```css
#page-map-header {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  height: 80px;
  color: white;
  background-color: darkblue;
}

```