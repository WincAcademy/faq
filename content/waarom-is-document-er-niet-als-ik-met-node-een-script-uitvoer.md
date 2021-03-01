+++
title = "Waarom is `document` er niet als ik met node een script uitvoer?"
extra.tags =[ "javascript",]
created = "Feb 13, 2020 2:51 PM"
+++
# Waarom is `document` er niet als ik met node een script uitvoer?
Als je in een omgeving zit waar je een webpagina hebt (de DOM dus) dan kun je mbv document met de DOM dingen doen. Dat kan in een JavaScript file of in de console van de developer tools van je browser.

Als je in een omgeving zit waar je géén webpagina hebt (als je een JavaScript file met node uitvoert op de command line) dan is er géén DOM en is document niet aanwezig en dus undefined.

(Je kan wel zelf een variabele met de naam document maken, maar dat is dan gewoon een variabele net als alle anderen. Daarnaast is het ook heel verwarrend 😵)