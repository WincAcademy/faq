+++
title = "Waarom wordt mijn css file overschreven? (Sass)"
extra.tags =[ "css",]
created = "Aug 27, 2020 10:59 AM"
+++
# Waarom wordt mijn css file overschreven? (Sass)


Als je een `foo.scss` bestand maakt en je zet je Sass compiler aan dan maakt de compiler `foo.css`. Als die al bestaat dan wordt die overschreven.

Je kan in principe `.css` bestanden en `.scss` bestanden naast elkaar hebben staan.

Bijvoorbeeld:

- `reset.css`
- `basic.css`
- `style.scss`
- `style.css` (automatisch gegenereerd uit style.scss)

Je wil dan uiteraard niet met de hand gaan schrijven in `style.css` , alle handmatige wijzigingen daarin worden elke keer overschreven als je Sass compiler draait.