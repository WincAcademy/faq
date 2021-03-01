+++
title = "Git in VSCode zegt dat ik 5000+ files track, wat is er aan de hand?!?"
extra.tags =[ "git",]
created = "May 11, 2020 2:23 PM"
+++
# Git in VSCode zegt dat ik 5000+ files track, wat is er aan de hand?!?


Git kan heel veel files aan.

Git in VSCode kan minder files aan, omdat VSCode ze allemaal moet laten zien, dus als er ineens heel veel files in je repository staan dan gaat Git in VSCode klagen.

Oplossing:

1. ga met je terminal naar je repository (op je harde schijf)
2. doe een `git status`
3. je krijgt nu een lijst van alle files te zien waar git verandering in ziet
4. waarschijnlijk staan hier heel veel files in die je **niet** in je repository wil
5. de reden hiervoor is waarschijnlijk dat je `git init` hebt gedaan op de verkeerde plek (namelijk ergens 'hogerop' in je computer, in `Documents` bijvoorbeeld. Git weet niet of dat een goeie plek is of niet en zal dus (bijvoorbeeld) van je hele `Documents` map, met duizenden files, een repository proberen te maken
6. we gaan nu uitzoeken wat de 'root' van de repository is
7. ga een map omhoog (met `cd ..`)
8. doe weer `git status`
9. krijg je nu een antwoord van git? ja → dan zit je nog steeds in de repository, ga naar stap 7
10. krijg je geen antwoord van git, dan is de laatste map van stap 7 de map waar je git repository in zit
11. we gaan nu je git repository verwijderen, **maar niet je files**
12. je git repository is een directory die `.git` heet, die directory (en **alleen** die directory!) kun je deleten
13. zie je de `.git` directory niet? [kijk hier hoe je dit soort verborgen files wel kan zien](https://www.notion.so/Hoe-kan-ik-verborgen-files-dotfiles-zien-07188638fb6145e2b188ed78e3f10ee0)
14. laatste stap: maak je git repository nu op de *goeie* plek met `git init`