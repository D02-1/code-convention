# Code-Convention für den Unterricht

Wenn du den Richtlinien in diesem Dokument folgst, 
stellst du sicher das jeder der Mitschüler und Tutoren deinen Code lesen kann.

> Der hier beschriebene "Code-Style" leitet sich von meiner persönlichen "Code-Convention" ab, die ich seit Jahren benutze, durch das Benutzen dieser Convention lernt ihr wie euer Code professionell aussieht, einfach zu lesen ist, und in Teams ohne probleme benutzt, erweitert, oder verändert werden kann.
>
> *- Frederik Reich* 
>

## Inhalt

1. [JavaScript](#-1-javascript)
    1. [Brackets](#-11-brackets)
    2. [Strings](#12-strings)
    3. [Indentation](#13-indentation)
    4. [Namen](#14-namen)
    5. [Semikolon](#15-semikolon)
    5. [Leerzeichen](#16-leerzeichen)
    5. [Variabeln](#17-variabeln)
2. [HTML](#2-html)
3. [CSS](#3-css)

## 1. JavaScript

### 1.1. Brackets

([Zurück zum Anfang](#-inhalt))

Brackets (Geschwungene Klammern) setzt du vorzugsweise in eine eigene Zeile:

```js
// Falsch:
function beispielFunktion() {
    console.log('Dies ist ein Beispiel');
}

if(value < 5) {
    console.log('value ist weniger als 5');
} else {
    console.log('value ist mehr als 5');
}

// Richtig:
function beispielFunktion()
{
    console.log('Dies ist ein Beispiel');
}

if(value < 5)
{
    console.log('value ist weniger als 5');
}
else
{
    console.log('value ist mehr als 5');
}
```

### 1.2. Strings

([Zurück zum Anfang](#-inhalt))

Bei Strings nutzt Du vorwiegend Single-Quotes:
```js
// Falsch:
"Dies ist ein String";

// Richtig:
'Dies ist ein String';
```

### 1.3. Indentation

([Zurück zum Anfang](#-inhalt))

Innerhalb eines code-blocks, indentierst du deinen code mit 4 leerzeichen (oder einem Tabulator).
```js
/// Falsch:
function beispielFunktion() {
console.log('Dies ist ein Beispiel');
}

if(value < 5) {
console.log('value ist weniger als 5');
} else {
console.log('value ist mehr als 5');
}

/// Richtig:
function beispielFunktion()
{
    console.log('Dies ist ein Beispiel');
}

if(value < 5)
{
    console.log('value ist weniger als 5');
}
else
{
    console.log('value ist mehr als 5');
}
```

### 1.4. Namen

([Zurück zum Anfang](#-inhalt))

Variablennamen, sowie Funktionennamen oder Methodennamen schreibst du in `camelCase`, Klassen in `PascalCase`:
```js
// Falsch:
var NewVariable;
var NEW_VARIABLE;
var New_Variable;
var _newVariable;
var _NewVariable;

_newfunction();
NEWFUNCTION();
new_Function();
New_Function();
NewFunction();

// Richtig:
const newVariable = 5;

newFunction();
```

Da du bei einem Boolean eine frage stellst, also ob etwas wahr, oder falsch ist, macht es sinn, dies im Namen der Variable wiederzuspiegeln:

```js
// Falsch:
const visible = true;
const equal = false;
const encryption = true;

// Richtig:
const isVisible = true;
const areEqual = false;
const hasEncryption = true;
```

### 1.5 Semikolon

([Zurück zum Anfang](#-inhalt))

Du beendest jedes Kommando mit einem Semikolon:
```js
// Falsch:
var testValue = 5

testValue + 8

// Richtig:
let testValue = 5;

testValue + 8;
```

### 1.6 Leerzeichen

([Zurück zum Anfang](#-inhalt))

In Arrays und Objekten, vor und nach den den verschiedenen Werten, fügst du ein Leerzeichen ein, dies erhöht die leserlichkeit:
```js
// Falsch:
[a, b, c, d, e]
{a, b, c, d, e}

// Richtig
{ a, b, c, d, e }
[ a, b, c, d, e ]
```

Außerdem beendest du jede .js Datei mit einer leeren Zeile:

```js
// Falsch:
const outputValue = "Hello World";

console.log(outputValue);
```

```js
// Richtig
const outputValue = "Hello World";

console.log(outputValue);

```

### 1.7. Variabeln

([Zurück zum Anfang](#-inhalt))

Wenn du eine neue Variabel deklarierst, nutzt du vorzugsweise `const`. `let` nutzt du nur dann, wenn du dir sicher bist das der Wert der Variabel überschrieben werden kann, var nutzt du garnicht.
```js
// Falsch:
let testValue = 5; // oder auch var testValue = 5;
console.log(testValue);

// Richtig:
const testValue = 5;
console.log(testValue);

let testValue2 = 'Hallo';
testValue2 = 'Welt';
console.log(testValue2);
```

### 1.8. Comments

([Zurück zum Anfang](#-inhalt))

Wenn du deinen Code kommentierst, nutzt du bitte entweder Single-Line comments oder JSDoc comments.
```js
// Falsch:
/* Dies ist ein Kommentar */
/* 
Dies ist ein Kommentar
*/
/*
    Dies ist ein Kommentar
*/

// Richtig:
// Dies ist ein Kommentar

/***
 * Dies ist ein
 * Kommentar
 */
```

### 1.9 Methodenschlange

([Zurück zum Anfang](#-inhalt))

Wenn du mehrere Funktionen/Methoden auf einen Wert anwendest, trennst du sie beim Punkt und schreibst sie untereinander, mit 4 Leerstellen Abstand zum Rand (oder 1 Tab).
```js
// Falsch:
'Dies ist ein String'.methode1().methode1().methode1();

// Richtig:
'Dies ist ein String'
    .methode1()
    .methode1()
    .methode1();
```

Andere arten von schlagen, wie zum beispiel den ternary operator, schreiben wir in eine zeile, solange er nicht zu lang wird.
```js
// Falsch:
const ternaryCheck =
testBool ? 
'(Boolean) Dies ist wahr' // IF 
: 
'(Boolean) Dies ist falsch'; // ELSE

// Richtig:
const ternaryCheck = testBool ? '(Boolean) Dies ist wahr' : '(Boolean) Dies ist falsch';
```

### 1.10. Konsole

([Zurück zum Anfang](#-inhalt))

Wenn du etwas in der Konsole ausgeben willst, 
zum Beispiel etwas aus einer Übungsaufgabe, 
dann legst du es vorher in einer Variable ab und gibst dann den wert mit console.log() aus.

```js
const testValue = "Hallo Welt";

console.log(testValue);
```

## 2. HTML
...

## 3. CSS
...
