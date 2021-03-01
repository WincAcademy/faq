+++
title = "Gebruik ik onclick? Of AddEventListerner?"
extra.tags =[ "dom", "javascript",]
created = "Feb 10, 2020 1:36 PM"
+++
# Gebruik ik onclick? Of AddEventListerner?

Gebruik addEventListerener. Klik voor meer info

Je hebt onclick en/of addEventListener door elkaar gebruikt. 

Beide werken, alleen zijn er wat voor en nadelen waar je van moet weten.

Sommige browsers ondersteunen “onclick” bijvoorbeeld niet. 
Check nog even het verschil.[https://caniuse.com/#search=onclick](https://caniuse.com/#search=onclick)

We raden je aan om consistent **addEventListener** te gebruiken, vanwege de browser compatibility 
[https://www.notion.so/wincacademy/JS-Adding-and-removing-classes-on-Browser-Event-58dfc8eece7849fc800589b00bdeec7f#618dc9d821a745ffab6b0d7a8411db76](https://www.notion.so/wincacademy/JS-Adding-and-removing-classes-on-Browser-Event-58dfc8eece7849fc800589b00bdeec7f#618dc9d821a745ffab6b0d7a8411db76)

[DOM: Browser Events ](https://www.notion.so/DOM-Browser-Events-1060d28629a541f6a39ad2e385b1edbf)