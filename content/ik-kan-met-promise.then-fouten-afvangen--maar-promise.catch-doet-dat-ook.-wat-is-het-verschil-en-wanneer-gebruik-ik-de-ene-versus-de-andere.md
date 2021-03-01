+++
title = "Ik kan met promise.then fouten afvangen, maar promise.catch doet dat ook. Wat is het verschil en wanneer gebruik ik de ene versus de andere?"
extra.tags =[ "javascript", "async",]
created = "Dec 17, 2019 2:24 PM"
+++
# wanneer gebruik ik promise.then versus promise.catch?
Als je een foutafhandelfunctie meegeeft aan .then dan vangt die alleen de error af voor die ene promise. Als je maar 1 promise gebruikt dan is dat handig.

Als je promises gaat chainen dan is het handig om .catch te gebruiken, die vangt dan alle errors af van alle daarvoor gechainde promises. Dan hoef je je errorafvang functie niet herhaaldelijk door te geven.

Zie https://github.com/WincAcademy/gists/tree/master/promises_vraag1