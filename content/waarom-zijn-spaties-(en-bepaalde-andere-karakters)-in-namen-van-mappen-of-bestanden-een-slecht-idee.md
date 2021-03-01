+++
title = "Waarom zijn spaties (en bepaalde andere karakters) in namen van mappen of bestanden een slecht idee?"
extra.tags =[ "praktisch",]
created = "Jan 7, 2020 9:37 AM"
+++
# Waarom zijn spaties (en bepaalde andere karakters) in namen van mappen of bestanden een slecht idee?
Als je als consument met computers werkt is het heel makkelijk om foldernamen aan te maken met spaties erin: Vakantiefoto's Spanje 2019.

Waarom zijn dit soort namen nou onhandig als je code schrijft?

Daar zijn een paar redenen voor:

1
Spaties in URLs zien er lelijk uit: %20 dus als je directorynaam een spatie heeft en je ziet die directory in de URL dan krijg je dat soort dingen in je URL. Voor andere 'moeilijke' karakters geldt dat ook. https://www.w3schools.com/tags/ref_urlencode.ASP

2
Als je met de command line werkt (wat je steeds meer zult gaan doen) dan is het vervelend om de hele tijd met spaties of andere karakters te werken. Je moet dan de spaties of andere karakters 'escapen' en dat kost extra tijd en nadenkwerk als je commando's aan het geven bent.

3
Sommige (oudere) systemen kunnen minder goed omgaan met spaties en bepaalde speciale karakters. Je zal daar misschien niet nu direct tegenaan lopen, maar als je er een keer tegenaan loopt zal dat precies op een moment zijn dat je haast hebt. Je hebt dan geen tijd (over) om allerlei namen van je folders en bestanden aan te passen. Als je folders en bestanden zonder spaties of speciale karakters gebruikt voorkom je dat je dat probleem ooit hebt.