+++
title = "Waarom is het niet handig 'gegenereerde code' te committen in Git?"
extra.tags =[ "git", "praktisch",]
created = "Nov 30, 2020 10:55 AM"
+++
# Waarom is het niet handig 'gegenereerde code' te committen in Git?


De vuistregel is eigenlijk: 

> In je repository moet alleen de informatie/code staan die nodig is om aan je project te werken.

Dit betekent dus dat als je Sass of Less gebruikt je alleen de originele files wil opslaan en dus **niet** de gegenereerde CSS files en ook niet de .css.map files.

## Waarom?

Als je commits bekijkt in de history van je repository wil je alleen de relevante veranderingen zien. Als je project op een of andere manier code genereert dan komen die veranderingen ook soms mee in de commits. Dat maakt commits 'noisy' omdat je dan op het oog moet gaan onderscheiden wat wel en niet belangrijk is.

## Hoe?

De oplossing is gelukkig simpel: gebruik `.gitignore` om gegenereerde files of hele directories met gegenereerde files te negeren.