+++
title = "Waarom werkt mijn CSS transition niet met display:none?"
extra.tags =[ "css",]
created = "Aug 27, 2020 8:52 AM"
+++
# Waarom werkt mijn CSS transition niet met display:none?


Om een transition te kunnen maken moet de browser een pad kunnen berekenen tussen punt A en punt B.

- Bij een transform in positie is dat logisch: een rechte lijn.
- Bij een transform in kleur is dat te berekenen: alle tussenkleuren
- Bij een transform in transparantie (opacity) is dat: van transparantie A naar B (0 naar 100 bijv).

Maar als een element niet zichtbaar is: met `display: none` en het moet dan naar `display: block` of een andere waarde dan is er niet echt een pad te vinden. De display property is als een lichtknopje: aan of uit. En veel andere properties zijn als een dimmer: met allemaal tussenstanden.

Als je elementen soepel wil laten verschijnen en verdwijnen maak dan gebruik van de opacity property.