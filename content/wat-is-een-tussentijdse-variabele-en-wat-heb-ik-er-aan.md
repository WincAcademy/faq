+++
title = "Wat is een tussentijdse variabele en wat heb ik er aan?"
extra.tags =[ "javascript",]
created = "Sep 23, 2020 5:09 PM"
+++
# Wat is een tussentijdse variabele en wat heb ik er aan?


In code is het mogelijk om heel veel dingen op elkaar te proppen en in elkaar te schuiven. Daar kan je code moeilijk leesbaar van worden. Om dit tegen te gaan is het (soms) handig om gebruik te maken van tijdelijke variabelen. Als je wat beter wordt in programmeren zul je deze 'kruk' wat minder vaak nodig hebben, maar het is goed om het als optie te hebben.

Een voorbeeld van een te 'in elkaar gedrukte' functie:

```js
const getRandomItem = arr => arr[Math.floor(Math.random() * arr.length)];

const beatles = ['John', 'Paul', 'George', 'Ringo', 'Kanye'];
console.log(getRandomItem(beatles));
```

Hieronder dezelfde code maar dan met een tijdelijke variabele er tussen waardoor de code wat makkelijker leesbaar wordt:

```js
const getRandomItem = arr => {
    const randomIndex = Math.floor(Math.random() * arr.length);
    return arr[randomIndex];
};

const beatles = ['John', 'Paul', 'George', 'Ringo', 'Kanye'];
console.log(getRandomItem(beatles));
```