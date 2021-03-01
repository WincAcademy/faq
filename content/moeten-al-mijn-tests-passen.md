+++
title = "Moeten al mijn tests passen?"
extra.tags =[ "testen",]
created = "Aug 31, 2020 3:19 PM"
+++
# Moeten al mijn tests passen?


Het is misschien goed om eerst even terug te stappen naar 'waarom hebben we tests?'

we hebben tests om te bewijzen dat onze code doet wat we willen dat het doet.

Als je code en tests voor die code aan het schrijven bent is het logisch dat niet de hele tijd al je tests passen.

1. Het is altijd goed om voordat je begint met werken eerst al je tests te draaien.
2. Als je tests snel genoeg draaien (bijvoorbeeld in minder dan 2 seconden) dan kun je ze de hele tijd draaien.
3. Stel je voor: je wil code schrijven om 'een boterham met pindakaas te maken'.
4. Je schrijft hier eerst een test voor.
5. Die test zal in eerste instantie *niet* passen, dat is dan nu de enige test die niet passed
6. Als je vervolgens code schrijft zodat de test *wel* passed passen al je tests weer.
7. Je kan nu *refactoren*, je code dus wat netter maken terwijl je tests blijven passen
8. Ga terug naar stap 3

(Je kan in stap 4 ook meerdere tests schrijven.)