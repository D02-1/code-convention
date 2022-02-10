# Linter

Ich habe der code-convention einen linter hinzugefügt, damit es euch einfacher fällt meiner code convention zu folgen, da dieser linter sie forciert. 

die regeln die ich angewandt habe, findet ihr in der json datei im ordner "linter" und wie sie aufgebaut sind, findet ihr hier:

https://eslint.org/docs/rules/

## Wie nutze ich den linter?

Installiere dir in vscode das plugin "eslint", danach kannst du bei jedem projekt `npm install -D eslint` machen und die datei `.eslintrc.json` aus dem linter verzeichnis in diesem repo in den root ordner deines gewünschten projektes schieben.

## Wir funktioniert der linter?
eslint wird überprüfen ob du dich an meine code convention hälst, sollte dies nicht der fall sein, werden fehler rot unterstrichen, wenn du mit der maus über das unterstrichene gehst, wird es dir sagen was du falsch gemacht hast.

## Wie kann ich den linter konstant beim entwickeln nutzen:
wenn wir in der package.json angeben, das wir den linter zusammen mit nodemon verwenden wollen, wird jedes mal wenn die app neu gestartet wird, mit eslint überprüft ob euer code sauber ist. sollte dies nicht der fall sein, wird node crashen.

dazu benötigen wir eine anpassung unseres "start:dev" befehls:
`"start:dev": "nodemon --exec 'eslint src/** && node ./src/index.js'"`

(damit nodemon zugriffsrechte auf exekutionsebene hat, muss es global installiert sein)

## Werde ich code, der nicht erfolgreich gelintet wurde lesen?
nein.
