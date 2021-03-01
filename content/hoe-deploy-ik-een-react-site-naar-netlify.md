+++
title = "Hoe deploy ik een React site naar Netlify?"
extra.tags =[ "netlify", "react",]
created = "Jul 8, 2020 2:05 PM"
+++
# Hoe deploy ik een React site naar Netlify?


Het korte antwoord: gebruik [netlify-cli](https://docs.netlify.com/cli/get-started/).

Je kan in [deze post van Netlify](https://www.netlify.com/blog/2016/07/22/deploy-react-apps-in-less-than-30-seconds/) lezen hoe je dat gebruikt.

Let op:

- gebruik create-react-app zoals je het altijd doet (zie [deze FAQ](https://www.notion.so/Hoe-begin-ik-met-create-react-app-e66464cb12d746ef9f87859a4edb3a9d))
- het installeren van netlify-cli duurt best lang: wees geduldig, zet even een kopje thee of koffie
- zorg dat je een account hebt bij Netlify
- voordat je netlify-cli kan gebruiken moet je je eerst authenticeren bij Netlify, daar vraagt netlify-cli zelf om de eerste keer
- deploy alleen de `build` folder