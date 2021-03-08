+++
title = "Gebruik ik onclick? Of AddEventListerner?"
extra.tags =[ "dom", "javascript",]
created = "Feb 10, 2020 1:36 PM"
+++
# Gebruik ik onclick? Of AddEventListerner?

Gebruik addEventListerener.

Heb je onclick en/of addEventListener door elkaar gebruikt? Beide werken,
alleen zijn er wat voor en nadelen waar je van moet weten. Sommige browsers
ondersteunen “onclick” bijvoorbeeld niet.  Check nog even het
verschil.[https://caniuse.com/#search=onclick](https://caniuse.com/#search=onclick)
We raden je aan om consistent **addEventListener** te gebruiken, vanwege de
browser compatibility.
