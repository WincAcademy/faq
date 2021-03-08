+++
title = "Wat is het verschil tussen .forEach() en .map()?"
extra.tags =[ "javascript",]
created = "Jun 24, 2020 2:53 PM"
+++
# Wat is het verschil tussen .forEach() en .map()?


## Het korte antwoord

- wil je een nieuw array maken? ➡️ `array.map()`
- wil je loopen zonder een nieuw array te maken? ➡️ `array.forEach()`

## Het lange antwoord

`array.forEach()` gebruik je vooral als vervanging van de standaard 'loopjes' dus de for loop en de while loop.  In de `array.forEach()` loop geef je dan een stukje code mee die voor elk item in de array wordt uitgevoerd. Nadat dit stukje code voor elk item uit de array is uitgevoerd, zal de `array.forEach()` functie altijd `undefined` teruggeven als return value. Dit komt omdat er niks wordt 'teruggegeven', er wordt alleen iets 'uitgevoerd'.

Voorbeeld:

```js
const myArray = [1, 2, 3];

myArray.forEach(arrayItem => {
	console.log('Hallo, de waarde van de huidige loop is', arrayItem);
})

// Verwachtte uitkomst:
// 'Hallo, de waarde van de huidige loop is 1'
// 'Hallo, de waarde van de huidige loop is 2'
// 'Hallo, de waarde van de huidige loop is 3'
// Return value: undefined
```

`array.map()` gebruik je als je een nieuwe array wilt creëren op basis van een bestaande array. Deze heeft wel altijd een return value: namelijk de nieuwe array.

Voorbeeld:

```js
const myArray = [1, 2, 3];

const doubleValueArray = myArray.map(arrayItem => arrayItem * 2);

console.log(doubleValueArray);

// Verwachte uitkomst:
// [2, 4, 6]
```

Het heeft dus weinig zin om een nieuwe variabele te assignen aan een forEach loop, zoals op deze manier:

```js
const doubleValueArray = array => array.forEach(element => {
    console.log(element *2);
});

console.log(doubleArrayValues([1, 2, 3]));
// undefined
```

Omdat de `forEach()` loop uit zichzelf geen nieuwe array returned, krijg je hier als return value `undefined`. Je schrijft hier namelijk een functie genaamd `doubleValueArray` die eigenlijk precies hetzelfde doet als wat de `array.forEach()` functie doet. Dat is dus overbodig.

Wel is het goed om in gedachten te houden dat je met de `array.orEach()` functie alles kan doen wat je met een `.map()` functie doet, maar dan zou je er veel meer code omheen moeten schrijven. 

Check voor een nog uitgebreider antwoord de volgende link: [https://stackoverflow.com/questions/34426458/javascript-difference-between-foreach-and-map#34426481](https://stackoverflow.com/questions/34426458/javascript-difference-between-foreach-and-map#34426481)