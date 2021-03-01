+++
title = "Wat is het verschil tussen const, let en var?"
extra.tags =[ "javascript",]
created = "Feb 5, 2020 10:08 AM"
+++
# Wat is het verschil tussen const, let en var?

We gebruiken const, let en var om nieuwe variabelen te maken. Ze werken alle drie net iets anders.

`const` gebruiken we om een variabele te maken die altijd dezelfde waarde moet hebben. Zoals bijvoorbeeld het aantal maanden in een jaar, dat is altijd 12, niet de ene keer 11 en de andere keer 12.
const monthsInYear = 12;

`let` gebruiken we om een variabele te maken die van waarde kan veranderen.
Een voorbeeld is de rekening in een restaurant:
let rekeningTotaal = 0;
rekeningTotaal = rekeningTotaal + 10;
rekeningTotaal = rekeningTotaal + 33;
rekeningTotaal = rekeningTotaal + 4;

var is de oude vorm van `let`, die zul je nog wel tegenkomen op het internet. `var` werkt een klein beetje anders dan `let` maar die details mag je zelf uitzoeken :-)

Wil je een ontzettend uitgebreide (en best complexe) uitleg? -->
https://tylermcginnis.com/var-let-const/