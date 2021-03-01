+++
title = "Wat is [Object object]?"
extra.tags =[ "html", "javascript",]
created = "Jan 16, 2020 11:01 AM"
+++
# Wat is [Object object] ?
Je kan deze vreemde string tegenkomen als je JavaScript values in HTML stopt. Als zo'n value een string of een nummer is dan gaat het goed: <div class='hoi'> of <div id='5'>. Maar als je (per ongeluk) een JavaScript object of array daarin stopt dan zet JavaScript dat automatisch voor je om in een string, die string is dan [Object object].

Want denk maar na, hoe zou een JavaScript object in HTML eruit moeten zien? Zoiets als dit kan nl niet :-)

Dit kan dus niet:
<div class='{a: 45}'>

Als je echt zeker weet dat je dit nodig hebt, dan kun je https://developer.mozilla.org/en-US/docs/Learn/HTML/Howto/Use_data_attributes gebruiken en dan https://stackoverflow.com/a/20406735.