+++
title = "Waarom zijn array methods meestal handiger dan loops?"
extra.tags =[ "javascript",]
created = "Feb 18, 2020 2:41 PM"
+++
# Waarom zijn array methods meestal handiger dan loops?


Je kan met array methods en met for loops precies dezelfde dingen gedaan krijgen.

Maar behalve iets 'gedaan krijgen' is het ook belangrijk dat je code goed leesbaar is, dat jij of iemand anders die naar je code kijkt snel(ler) ziet wat er aan de hand is. Makkelijk leesbare code heeft ook minder snel bugs erin.

Het gebruiken van array methods in plaats van loops is een goede manier om je code makkelijker leesbaar te krijgen. Door gebruik te maken van bepaalde array methods hoef je niet zelf de code te schrijven om 

1. iets uit een array te halen
2. een nieuw array aan te maken
3. een array te updaten
4. te checken of je aan het einde van een array bent

En in al die dingen kun je (en *zul* je fouten maken).

Voorbeeld:

- we hebben een array
- we willen alleen de even nummers overhouden
- daar willen we het kwadraat van
- en dat nieuwe array dan console.loggen

```jsx
const arr = [1, 2, 3, 4, 5, 6, 7, 8];
const newArray = [];
for (let i = 0; i < arr.length; i++) {
  if (arr[i] % 2 === 0) {
    newArray.push(arr[i] * arr[i]);
  }
}
console.log(newArray);
```

Als de berekeningen die je doet in een aparte functie staan dan ziet het er met for loops zo uit:

```jsx
const arr = [1, 2, 3, 4, 5, 6, 7, 8];
const isEven = number => number % 2 === 0;
const calculateSquare = number => number * number;

const newArray = [];
for (let i = 0; i < arr.length; i++) {
  if (isEven(arr[i])) {
    newArray.push(calculateSquare(arr[i]));
  }
}
console.log(newArray)
```

Met array methods ziet het er al meteen wat 'schoner' uit:

```jsx
const arr = [1, 2, 3, 4, 5, 6, 7, 8];
const evenNumbers = arr.filter(number => number % 2 === 0);
const squares = evenNumbers.map(number => number * number);
console.log(squares);
```

Je kan de array methods ook wat compacter opschrijven:

```jsx
const arr = [1, 2, 3, 4, 5, 6, 7, 8];
console.log(arr.filter(n => n % 2 === 0).map(n => n * n));
```

Als de berekeningen die je doet in een aparte functie staan ziet de code met array methods er nog 'cleaner uit':

```jsx
const arr = [1, 2, 3, 4, 5, 6, 7, 8];
const isEven = number => number % 2 === 0;
const calculateSquare = number => number * number;
console.log(arr.filter(isEven).map(calculateSquare));
```

Bij deze laatste variant is het makkelijk om de kleine 'utility functions' die je hebt gemaakt ergens anders weer opnieuw te gebruiken.