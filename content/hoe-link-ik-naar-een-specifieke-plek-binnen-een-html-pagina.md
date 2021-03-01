+++
title = "Hoe link ik naar een specifieke plek binnen een HTML pagina?"
extra.tags =[ "html",]
created = "Aug 27, 2020 2:23 PM"
+++
# Hoe link ik naar een specifieke plek binnen een HTML pagina?


Een #in-page-link kan gebruikt worden om naar een specifieke positie in de pagina te gaan. Dit wordt vaak gebruikt om te voorkomen dat de gebruiker moet scrollen om de juiste informatie te vinden. 

Om dit te implementeren heb je een `<a>` tag nodig en een element met een specifieke id.

```
<a href='#mijn-in-page-link'>
```

En dan op de plek waar je naartoe kan springen:

```
<div id='mijn-in-page-link'>
```

Voor meer info zie:

[: The Anchor element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a#Linking_to_an_element_on_the_same_page)