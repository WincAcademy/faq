+++
title = "Hoe gebruik ik meerdere JavaScript files?"
extra.tags =[ "javascript",]
created = "Sep 30, 2020 10:41 AM"
+++
# Hoe gebruik ik meerdere JavaScript files?


Als je wat meer code gaat schrijven kan het handig en verstandig zijn om je code op te splitsen in meerdere files.

Dat kan op meerdere manieren. Kies wel altijd maar één manier :-)

## In een HTML pagina

Als je een HTML pagina hebt dan is de simpelste manier om meerdere JavaScript files in te laden de volgende. In de `<head>`van je pagina zet je twee `<script>` tags, zoals hieronder:

```html
<script defer src='script1.js'></script>
<script defer src='script2.js'></script>
```

Let op de volgorde, als je in `script2.js` iets wil gebruiken dat in `script1.js` staat moet je ze ook in die volgorde in je HTML zetten.

## In een Node.js script

In een Node.js script, zonder website of HTML in de buurt, kun je geen HTML tags gebruiken.

We draaien altijd één script met Node, laten we die `main.js` noemen. Dus dat wordt:

`$ node main.js`

Maar als we nou een andere JavaScript file hebben waarvan we willen dat `main.js` daar gebruik van kan maken dan moeten we twee stappen nemen:

1. de file die we willen inladen moet iets 'exporten', zie onder
2. de file die een andere file wil inladen moet 'requiren'

```jsx
// vegetables.js
const vegetables = ['peas', 'corn', 'potatoes'];

module.exports = {vegetables};
```

```jsx
// main.js
const vegetablesModule = require('./vegetables.js');
const vegetables = vegetablesModule.vegetables;

console.log('De eerste groente is:');
console.log(vegetables[0]);
```

## In een React applicatie

In een React applicatie volg je het patroon dat je ziet als je `create-react-app` draait.