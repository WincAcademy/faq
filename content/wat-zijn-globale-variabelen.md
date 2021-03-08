+++
title = "Wat zijn globale variabelen?"
extra.tags =[ "javascript",]
created = "Feb 18, 2020 12:19 PM"
+++
# Wat zijn globale variabelen?


Het korte antwoord: globale variabelen zijn variabelen die *buiten* functies zijn gemaakt. Vanwege de 'scope' regels in JavaScript kan alle code bij die globale variabelen en ze dus ook lezen én aanpassen. Voorbeeld:

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

Zie ook 

[JS: Scoping: global vs local scope](https://www.notion.so/JS-Scoping-global-vs-local-scope-e38aed4fecae4ce48c5736013319935c)

[Waarom zijn globale variabelen gevaarlijk?](@/waarom-zijn-globale-variabelen-gevaarlijk.md)

Hoe voorkom je dat je globale variabelen nodig hebt? →

[Waarom is het goed om functies alles mee te geven dat ze nodig hebben?](@/waarom-is-het-goed-om-functies-alles-mee-te-geven-dat-ze-nodig-hebben.md)