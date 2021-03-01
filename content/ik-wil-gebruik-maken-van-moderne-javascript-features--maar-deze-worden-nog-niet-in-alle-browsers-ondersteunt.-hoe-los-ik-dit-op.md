+++
title = "Ik wil gebruik maken van moderne JavaScript features, maar deze worden nog niet in alle browsers ondersteunt. Hoe los ik dit op?"
extra.tags =[ "javascript",]
created = "Nov 23, 2020 2:20 PM"
+++
# Ik wil gebruik maken van moderne JavaScript features, maar deze worden nog niet in alle browsers ondersteunt. Hoe los ik dit op?
Polyfills

JavaScript, en de specificatie waar het aan voldoet (ECMAScript) veranderen voortdurend, en ontvangen dan ook wel eens nieuwe features. Deze features moeten door de ontwikkelaars van browsers ondersteund worden, en dit kan soms wel eens lang duren, of het gebeurt überhaupt niet.

Het kan dus voorkomen dat jij als programmeur een feature van de laatste versie van JavaScript wil gebruiken in jouw code, maar dat deze feature (nog niet) ondersteund wordt door (alle) browsers waarop jij wil dat jouw code kan draaien. In dit geval zal je een stukje code moeten schrijven/gebruiken die de ondersteuning als het ware handmatig toevoegd. Zo'n stukje code heet een `polyfill`.

## Wanneer is dit nodig?

Om erachter te komen of je een polyfill nodig hebt voor het gebruik van een bepaalde feature kun je beslissen welke browsers (of versies van de browsers) je wilt ondersteunen.
Als jij werkt aan een website waar miljoenen mensen dagelijks afhankelijk van zijn is het misschien nog nodig om Internet Explorer van 2000 te ondersteunen, en zal een polyfill dus misschien nodig zijn. Als je echter bijvoorbeeld een website maakt voor jezelf en een aantal vrienden is het waarschijnlijk acceptabel om alleen de meest recente versies van je favoriete browser te ondersteunen, en dus zal een polyfill waarschijnlijk niet nodig zijn.

Om te zien welke browserversies welke features ondersteunen kun je kijken op websites als [caniuse.com](https://www.caniuse.com). Hier kun je bijvoorbeeld zoeken naar `Array.prototype.map` om te zien welke browsers de ingebouwde array-method `map` ondersteunen.

## Hoe maak/gebruik ik een polyfill?

Vaak zal de code van een polyfill al geschreven zijn door iemand anders. Deze code kun je dan opzoeken en toevoegen aan jouw code. Zorg er hierbij voor dat je deze code uitvoert voordat je gebruik maakt van de feature.

Om bijvoorbeeld `Array.prototype.map` te polyfill-en kun je naar [de MDN-pagina van map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) gaan. Hier staat een [kopje polyfill](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map#Polyfill), waar code te vinden is die je kunt gebruiken.

Als je een polyfill voor een bepaalde feature niet kan vinden op de desbetreffence MDN-pagina kun je ernaar googlen om te proberen dit ergens anders vandaan te halen. Als er online echt geen code te vinden is voor ene polyfill zul je deze code zelf moeten schrijven.

## Meer informatie

Voor meer informatie, zie o.a. de volgende links:
[https://developer.mozilla.org/en-US/docs/Glossary/Polyfill](https://developer.mozilla.org/en-US/docs/Glossary/Polyfill)

[https://javascript.info/polyfills](https://javascript.info/polyfills)

[https://www.google.com/search?q=polyfill](https://www.google.com/search?q=polyfill)