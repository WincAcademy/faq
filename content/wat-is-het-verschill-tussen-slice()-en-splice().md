+++
title = "Wat is het verschill tussen slice() en splice()"
extra.tags =[ "javascript",]
created = "Feb 12, 2020 10:17 AM"
+++
# Wat is het verschill tussen slice() en splice()?
Splice muteert de orginele array en Slice laat de orginele array onveranderd

Slice en Splice zijn standaard JavaScript Array methods. Voor beide methods zijn valide use-cases, maar belangrijk is dat je het verschil begrijpt (hint: **mutability**).

### Splice

```js
let array = [1, 2, 3, 4, 5];
let part = array.splice(2);

console.log(part); // outputs [3, 4, 5]
```

`.splice()` **muteert** de orginele array en geeft de waardes `[3, 4, 5]` terug als een array van nummers. Door de mutatie is de orginele array veranderd:

```js
console.log(array); // outputs [1, 2]
```

Raadpleeg de [documentatie van Array.splice](https://developer.mozilla.org/nl/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)

### Slice

```js
let array = [1, 2, 3, 4, 5];
let part = array.slice(2);

console.log(part); // outputs [3, 4, 5]
```

`.slice()` geeft de waardes `[3, 4, 5]` terug als een array van nummers. Door orginele array is onveranderd gebleven:

```js
console.log(array); // outputs [1, 2, 3, 4, 5]
```

Raadpleeg de [documentatie van Array.slice](https://developer.mozilla.org/nl/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)