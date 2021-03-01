+++
title = "Waarom is het niet handig een functie maar één keer te gebruiken?"
extra.tags =[ "javascript",]
created = "Mar 26, 2020 3:56 PM"
+++
# Waarom is het niet handig een functie maar één keer te gebruiken?


Functies zijn ontzettend handig en je gaat ze heel vaak gebruiken. Maar soms heb je geen functie nodig.

Sommige mensen willen nog wel eens dit soort code schrijven:

```jsx
const addEventListenerToButton = function() {
  const button = document.querySelector('button');
  button.addEventListener('click', function() {
    console.log('I was clicked');
  });
};
addEventListenerToButton();
```

Nu werkt die code wel, maar zo'n functie is (vaak) overbodig omdat we die functie:

- maar één keer aanroepen
- direct nadat we de functie maken.

Dus even terug naar 'waarom zou ik een functie gebruiken?'

Functies zijn handig als je:

- een stuk code meerdere keren wil gebruiken (zo blijft je code DRY)
- een stuk code *dynamisch* wil gebruiken, dus meerdere keren, maar elke keer nét een beetje anders
- je voor de duidelijkheid een aantal regels code een goede naam wil geven
- (en nog een aantal andere redenen die wat technischer zijn, zoals scope, functies-als-variabelen etc)

Het voorbeeld hierboven kan ook zo geschreven worden:

```jsx
const button = document.querySelector('button');
button.addEventListener('click', function() {
  console.log('I was clicked');
});
```