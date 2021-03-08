+++
title = "Hoe manipuleer ik mijn HTML met JavaScript?"
answer = "Door het gebruik van DOM-objecten"
extra.tags =[ "dom", "html",]
created = "Feb 26, 2020 10:39 AM"
+++

# Hoe manipuleer ik mijn HTML met JavaScript?

Bij het ontwikkelen van een website of app, zal je regelmatig de
documentstructuur van je site willen manipuleren. Dit doen we met het Document
Object Model (DOM). Met de API (objects en methodes) van het DOM kunnen we de
HTML van onze pagina manipuleren en maken we statische pagina's dynamisch.

Voordat je begint met het manipuleren van het DOM is het belangrijke om te
beginnen met een statische opzet. Zorg ervoor dat je eerst de gewenste HTML en
CSS uitschrijft voordat je interactie toevoegd. Denk goed na over welke HTML
elementen je gebruikt en wat het eindresultaat moet zijn.

## Praktijkvoorbeeld

Je gaat een nieuw winkelwagentje bouwen voor de webshop
[bell.com](http://bell.com/). De producten van de klant worden opgehaald via
een REST API en zijn tot je beschikking in de vorm van een JavaScript array.

De HTML structuur van het winkelwagentje ziet er als volg uit:

```html
<div class='cart'>
    <h3>Mijn winkelwagentje</h3>
    <ul class='products'></ul>
</div>
```

De array met producten ziet er als volgt uit:

```jsx
const products = [
    {
        name: 'Macbook Pro',
        price: 2849.99,
        brand: 'Apple'
    },
    {
        name: 'Windows Surface Pro',
        price: 2750.00,
        brand: 'Microsoft'
    },
    {
        name: 'Asus Ultrabook',
        price: 1680.80,
        brand: 'Asus'
    }
]
```

Nu kunnen we de DOM manipuleren met JavaScript zodat de producten van de klant worden getoond in het lijstje (`ul.products`) van het winkelwagentje:

```jsx
const itemsInCart = document.querySelector('.products');

// (1) loop door de producten
products.forEach((product) => {
    // (2) maak een nieuw <li> element aan
    const li = document.createElement('li');

    // (3) voeg de producttekst toe aan het element
    li.innerText = `${product.name} (€${product.price})`;

    // (4) voeg het element toe aan de lijst van het winkelwagentje
    itemsInCart.appendChild(li);
});
```

Het eindresultaat ziet er als volgt uit:

![winkelwagentje.png](@/winkelwagentje.png)

Dit is een simpel voorbeeld, maar de mogelijkheden zijn eindeloos. Door gebruik te maken van de DOM-objecten (zoals `document`) kunnen we verschillende methods aanroepen om elementen te selecteren, creëren en manipuleren. Exploreer en experimenteer!

## Handige links

Voor nog veel meer informatie over de DOM en hoe je daar dingen mee kan doen:

[JavaScript HTML DOM](https://www.w3schools.com/js/js_htmldom.asp)

[Documenten manipuleren](https://developer.mozilla.org/nl/docs/Learn/JavaScript/Client-side_web_APIs/Manipuleren_documenten)

[dom manipulation - YouTube](https://www.youtube.com/results?search_query=dom+manipulation)
