+++
title = "Deployen naar Netlify lukt niet, wat nu?"
answer = "Zie hieronder."
extra.tags =[ "netlify",]
created = "Dec 30, 2019 3:26 PM"
+++
# Netlify: Deployen naar Netlify lukt niet, wat nu?


Om Netlify te gebruiken **moet** je een map naar Netlify slepen met daar IN een file die index.html heet. 

👉 Sleep je de map, met daar IN een index.html file? Dus niet de file zelf? 
👉 Heet je html file `index.html`?

[Heet mijn file wel index.html?](@/heet-mijn-file-wel-index.html.md)

👉 Is je HTML pagina correct? Zitten er geen 'foutjes' in? 
👉 Zijn je files in de map opgeslagen?

Controleer de status van de Netlify drop app:

[Netlify Status](https://www.netlifystatus.com/)

Als je deze melding krijgt:

> “We’re having some trouble connecting you to Netlify. This error may be caused by an ad blocker or browser extension. You can try disabling blocking on this page or running in incognito”

👉 Maak een account aan bij Netlify (sign up)

Deployen gaat **fout** als je:

💣een bestand sleept in plaats van een map

💣een map erin sleept waar niet *direct* een `index.html` file in zit