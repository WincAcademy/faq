+++
title = "Wat is het verschil tussen === en == en welke moet ik gebruiken?"
extra.tags =[]
created = "Mar 19, 2020 12:08 PM"
+++
# Wat is het verschil tussen === en == en welke moet ik gebruiken?


Als je in JavaScript wil wetenof dingen hetzelfde zijn kun je dat doen met de zgn 'equality operators':

- `==` (ongeveer gelijk aan elkaar)
- `!=` (ongeveer niet gelijk aan elkaar)
- `===` (écht gelijk aan elkaar)
- `!==` (écht niet gelijk aan elkaar)

De laatste 2 noemen we de 'strict equality operators'.

Die eerste 2 zijn niet handig om te gebruiken. En wel om de volgende redenen.

```js
0 == False; // true
'' == False; // true
```

Je kan dus met `==` en `!=` er eigenlijk niet goed op rekenen dat dingen echt gelijk of ongelijk aan elkaar zijn. Voor een visueel overzicht van hoe 'rommelig' en inconsistent de non-strict equality operators zijn: 

[JS Comparison Table](https://dorey.github.io/JavaScript-Equality-Table/)

In de 2e tab van die pagina zie je ook hoe simpel en consistent het gebruik van de strict equality operator is.

Dus:

### Gebruik ALTIJD `===` en `!==`

Meer informatie:

[Comparisons](https://javascript.info/comparison#strict-equality)

[When is it OK to use == in JavaScript?](https://2ality.com/2011/12/strict-equality-exemptions.html)