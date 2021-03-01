+++
title = "React hoe bepaal ik de structuur van mijn state?"
extra.tags =[]
created = "Mar 10, 2020 12:46 PM"
+++
# React: hoe bepaal ik de structuur van mijn state?


Wanneer je een state gaan maken voor bijvoorbeeld de lil' spotify list, vraag je dan altijd af: welke entiteiten heb ik in mijn app? 

In ons geval: songs. 
1 Song heeft bepaalde eigenschappen en het is de bedoeling dat er meerdere songs in mijn state terecht gaan komen. 
1 song is dus 1 ding oftewel 1 entiteit. 
Songs zijn meerdere entiteiten, oftwel meerdere dingen. 

Conclusie:
1 song is een object. 
songs is een array van objecten.

Goed om te weten:
voel je altijd vrij om de structuur van je state aan te passen als je initiële plan niet heeft gewerkt. Het creeëren van een juiste datastructuur is een proces dat organisch ontwikkelt.