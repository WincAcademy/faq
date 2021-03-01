+++
title = "Een plaatje op mijn pagina werkt op mijn computer wel maar op Netlify niet"
extra.tags =[ "netlify",]
created = "Jan 2, 2020 1:32 PM"
+++
# Netlify: Een plaatje op mijn pagina werkt op mijn computer wel maar op Netlify niet

Grote kans dat dit komt door het volgende:

Als je in je HTML verwijst naar een plaatje (met de <img> tag) geef je het 'pad' naar dat plaatje op. 

Als het plaatje in dezelfde directory staat dan kun je de naam van het bestand opgeven: <img src='plaatje.jpg'/>

Als het plaatje in een subdirectory staat dan moet je een pad opgeven: <img src='images/plaatje.jpg'/>

Als het pad in je HTML verwijst naar een directory die alleen op je computer aanwezig is dan werkt dit wél op je computer maar niet ergens anders (zoals bijvoorbeeld op Netlify): <img src='C:\Documenten\Projecten\Winc\Opdracht3\images\plaatje.jpg'/>
Want Netlify 'weet' niet waar dit is: C:\Documenten\Projecten\Winc\Opdracht3\images\plaatje.jpg