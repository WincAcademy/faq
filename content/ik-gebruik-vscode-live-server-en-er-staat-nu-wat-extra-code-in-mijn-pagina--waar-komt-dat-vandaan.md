+++
title = "Ik gebruik VSCode Live Server en er staat nu wat extra code in mijn pagina, waar komt dat vandaan?"
extra.tags =[ "vscode",]
created = "Jun 23, 2020 2:24 PM"
+++
# Ik gebruik VSCode Live Server en er staat nu wat extra code in mijn pagina, waar komt dat vandaan?
De code van je pagina ziet er inderdaad wat anders uit als je deze met de Liveserver plugin van VSCode opent.

De reden daarvoor is de volgende:
Om deze functionaliteit te hebben moeten VSCode en de browser met elkaar kunnen praten. VSCode moet de browser namelijk kunnen vertellen: 'hey de HTML, CSS of JavaScript van de pagina is geupdate: herlaad de pagina'. Om ervoor te zorgen dat de browser kan luisteren naar VSCode wordt er wat extra JavaScript (en mss ook HTML) 'geïnjecteerd'. Als het goed is zou dat niet in de weg moeten zitten, maar als je het niet verwacht dan snap ik dat het er vreemd uitziet.