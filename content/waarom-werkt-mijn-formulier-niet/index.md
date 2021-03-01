+++
title = "Waarom werkt mijn formulier niet?"
answer = "zie onderstaand"
extra.tags =[ "netlify",]
created = "Dec 30, 2019 3:49 PM"
+++
# Netlify: mijn formulier werkt niet help?


Kan aan meerdere dingen liggen. Hier een checklist:

- Staat het attribute `data-netlify='true'` in je form? Ook geen typo?
- Heb je de homepage van Netlify al gerefresht nadat je een submission hebt gemaakt? Links onderin verschijnen je form submission zoals op het onderstaande screenshot.
- Zijn de rest van je **form attributes** correct zoals beschreven in de **documentatie van Netlify**?

    `<form name='contact' method='POST' data-netlify='true'>` 

- Heeft je form een button van het type 'submit'? Want anders weet het formulier niet hoe het verzonden moet worden 
`<button type='submit'>Send</button>`
- Je HTML moet helemaal kloppen: als er foutjes in je HTML zitten kan Netlify je formulier bijvoorbeeld niet accepteren. Check je HTML met de strengste linter: [https://validator.w3.org/#validate_by_input](https://validator.w3.org/#validate_by_input) en fix de fouten die daaruit komen.

Screenshot Netlify form submissions, met link onderin de recent form submissions:

![netlify-form.png](@/netlify-form.png)