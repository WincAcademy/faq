+++
title = "Kan ik beter let of const gebruiken voor een function expression?"
extra.tags =[ "javascript", "project",]
created = "Feb 10, 2020 1:46 PM"
+++
# Kan ik beter let of const gebruiken voor een function expression?

Lang antwoord kort: const.

Een functie kun je in een variabele stoppen. Dus gelden voor deze variabele de 'normale' regels voor const of let. Aangezien je de functie niet meer gaat veranderen of aanpassen, het is immers een vaste 'machine' waar je evt iets in stopt, en iets uitkomt. 
De parameters kunnen veranderen, maar de functie zelf niet. Oftewel: gebruik const.