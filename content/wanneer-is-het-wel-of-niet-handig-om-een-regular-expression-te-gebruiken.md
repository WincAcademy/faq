+++
title = "Wanneer is het wel of niet handig om een regular expression te gebruiken?"
extra.tags =[ "javascript", "python",]
created = "Nov 3, 2020 11:29 AM"
+++
# Wanneer is het wel of niet handig om een regular expression te gebruiken?


Regular expressions (regex) zijn hele krachtige tools. Je kan er heel veel mee. Maar omdat ze ook vrij complex zijn hebben ze ook een risico: je *denkt* dat je regex werkt maar je mist een paar 'edge cases'. Een edge case is een situatie waar je niet aan hebt gedacht waar je regex ook op moet werken.

De vuistregel is eigenlijk:

> Gebruik de simpelste tool voor het klusje.

Voorbeelden:

Als je wil weten of een string met 'abc' begint kun je dat doen met regex. Maar je hebt ook in JavaScript de `String.startsWith` methode. Die is veel simpeler.

Als je wil weten of een string uppercase of lowercase karakters bevat kun je dit doen:

```js
const name = 'Winc Academy';
const hasUpperCase = str => str.toLowerCase !== str;
const hasLowerCase = str => str.toUpperCase !== str;
```

Maar als je taak complexer wordt dan kan een regex wel het goede antwoord zijn.