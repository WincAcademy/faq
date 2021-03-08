+++
title = "Waarom zijn globale variabelen gevaarlijk?"
extra.tags =[ "javascript",]
created = "Feb 18, 2020 1:07 PM"
+++
# Waarom zijn globale variabelen gevaarlijk?


[Wat zijn globale variabelen?](@/wat-zijn-globale-variabelen.md)

Maar waarom zijn ze gevaarlijk?

Dat heeft te maken met *voorspelbaarheid.* Als je een functie aanroept wil je er van uit kunnen gaan dat die functie hetzelfde doet. Wat die functie *verandert* in de wereld of wat die functie *produceert* (terug geeft) moet makkelijk voorspelbaar zijn.

Als een functie gebruik maakt van globale variabelen dan moet je eerst weten wat die globale variabelen zijn voordat je kan *voorspellen* wat die functie precies gaat doen.

Anders gezegd, bij een functie die gebruik maakt van globale variabelen is het:

- moeilijk(er) te voorspellen wat die precies gaat doen
- moeilijker om over die functie en de code eromheen na te denken (omdat je altijd rekening moet houden met die global variables)
- testen van die functie een flink stuk moeilijker

Bij dit stuk code geeft `readFoo()` de 1e en 2e keer iets anders terug omdat we de global variable gebruiken.

```js
let foo = 3;

const readFoo = () => {
  console.log(foo);
};

const changeFoo = () => {
  foo = 30;
};

readFoo(); // 3
changeFoo();

// Heel
// Veel
// Andere
// Code

readFoo(); // 30
```

Maar hoe schrijf je je code dan? →

[Waarom is het goed om functies alles mee te geven dat ze nodig hebben?](@/waarom-is-het-goed-om-functies-alles-mee-te-geven-dat-ze-nodig-hebben.md)

[Hoe verander ik mijn code om geen globals meer te gebruiken?](@/hoe-verander-ik-mijn-code-om-geen-globals-meer-te-gebruiken.md)

## Lees meer

[](https://wiki.c2.com/?GlobalVariablesAreBad)