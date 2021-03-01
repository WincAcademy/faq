+++
title = "Mijn media query lijkt niet goed te werken op een telefoon of met mobile mode in de devtools, waarom niet?"
extra.tags =[ "css",]
created = "Sep 29, 2020 4:39 PM"
+++
# Mijn media query lijkt niet goed te werken op een telefoon of met mobile mode in de devtools, waarom niet?


In de basis zijn media queries die reageren op de breedte van je scherm in pixels relatief simpel:

- is het scherm breder dan X? ➡️ laad dan (ook) deze CSS
- is het scherm breder dan Y? ➡️ laad dan (ook) deze CSS

Maar je zal misschien gemerkt hebben dat de realiteit iets complexer is. De reden hiervoor is de volgende:

Er zijn nog steeds websites die van zichzelf *niet* handig zijn op een klein scherm. Als je die op een smal scherm zou laden dan zou het een super-onhandige site zijn. De browsers op telefoons hebben daarom een bepaalde standaard instelling: ze weten dat het scherm van je telefoon (bijvoorbeeld) 500px breed is, maar ze vertellen de website 'ik ben 1000px breed'. Zo kan een site die 1000px breed is toch getoond worden op een scherm van 500px, ze zoomen dan een stuk uit. 

Deze standaard instelling is voor de maker van een website die juist mooie mediaqueries geschreven heeft natuurlijk flink onhandig. Maar daar kun je wat aan doen: voeg deze HTML toe aan de <head> van je pagina:

```html
<meta name='viewport' content='width=device-width, initial-scale=1'>
```

Hoe dit precies werkt is een lang en wat technisch verhaal. Daar mag je in duiken, maar raak niet de weg kwijt :-) 

[Using the viewport meta tag to control layout on mobile browsers](https://developer.mozilla.org/en-US/docs/Mozilla/Mobile/Viewport_meta_tag)