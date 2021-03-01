+++
title = "Waarom is het goed om functies alles mee te geven dat ze nodig hebben?"
extra.tags =[ "javascript",]
created = "Feb 18, 2020 1:15 PM"
+++
# Waarom is het goed om functies alles mee te geven dat ze nodig hebben?


Lees eerst deze vraag:

[Waarom zijn globale variabelen gevaarlijk?](@/waarom-zijn-globale-variabelen-gevaarlijk.md)

Nu is het niet alleen zo dat globale variabelen gevaarlijk of onhandig kunnen zijn. Dat kan ook gelden in een meer 'lokale' scope. Zie dit voorbeeld:

```jsx
console.log('---');
const langeFunctie = () => {
  let bar = 5;

  const readBar = () => {
    console.log(bar);
  };

  const changeBar = () => {
    bar = 50;
  };

  readBar(); // 5
  changeBar();

  // Heel
  // Veel
  // Andere
  // Code

  readBar(); // 50
};

langeFunctie();
```

Hier is `bar` een lokale variabele. Maar de functie readBar kijkt als het ware om zich heen om diens werk te kunnen doen. Dus readBar kijkt *in de omliggende scope* voor bar.

Dan hebben we dus precies hetzelfde probleem als bij globale variabelen: het is moeilijk te voorspellen wat ze precies doen.

## Oplossing!

Om functies voorspelbaar te maken kunnen we iets vrij simpels doen:

geef de functie alle data mee die die functie nodig heeft om diens werk te kunnen doen

Als je dit doet:

- is het de lezer van je code (jij in een paar maanden) sneller duidelijk waar de data voor deze functie vandaan komt
- doet je functie altijd precies hetzelfde *als* de argumenten die je aan die functie geeft hetzelfde zijn
- is je functie veel makkelijker te testen

Conclusie: je code wordt veel voorspelbaarder.