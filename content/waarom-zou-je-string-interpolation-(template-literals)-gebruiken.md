+++
title = "waarom zou je string interpolation (template literals) gebruiken?"
extra.tags =[ "javascript",]
created = "Dec 17, 2019 11:54 AM"
+++
# waarom zou je string interpolation (template literals) gebruiken?


Dit is string interpolation: 

```js
let title = 'Mrs.';
let name = 'Doubtfire';
let greeting = `Dear ${title} ${name}`; // 'Dear Mrs. Doubtfire'
```

Als je strings en variabelen wil combineren tot één lange string kan dat het beste met 'string interpolation'.

Deze manier van strings en variabelen combineren is meestal leesbaarder en makkelijker onderhoudbaar dan bijv string concatenatie.

Meer info:
[https://campushippo.com/lessons/how-to-do-string-interpolation-with-javascript-7854ef9d](https://campushippo.com/lessons/how-to-do-string-interpolation-with-javascript-7854ef9d)

Hoe ze te gebruiken? →
[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)

⚠️ Let op: als je maar één string hebt kun je gewoon die string gebruiken dan hoef je niet te interpoleren:

```js
let name = 'Fresh Prince';
console.log(`${name}`); // 'Fresh Prince' (overbodig gebruik van interpolatie)
console.log(name); // 'Fresh Prince'
```