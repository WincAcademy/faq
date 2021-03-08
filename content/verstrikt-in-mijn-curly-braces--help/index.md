+++
title = "Verstrikt in mijn {curly braces}, help?!?"
answer = "Tips om ervoor te zorgen dat je jouw curly braces goed managed."
extra.tags =[ "project",]
created = "Feb 10, 2020 2:19 PM"
+++
# Verstrikt in mijn {curly braces}, help?!?


Curly braces mess is een chaos om in te werken. Je kunt heel lang vastzitten door een ontbrekende `}` of een ontbrekende `{` . Daarom hier een aantal tips om het te voorkomen: 

Tips: 

- Gebruik een linter die je meteen verteld als er iets mis is door een rood kringeltje onder de curly braces.
- Maak er een gewoonte van om elke keer als je een functie declareert of een if-statement neerzet, **meteen** de curly braces ook te sluiten. Daarna pas de inhoud te gaan vullen.
- **Indentation**. 
Juist formatteren van je bestanden en **indenten** van nieuwe loops/if-statements of functies kan je leven redden in curly brace chaos.
- Gebruik [een extension](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer-2) om op basis van kleur de open-en-sluit-accolades te zien

![curly-braces](@/curly-braces.png)

- Wanneer je bestand **niet** automatisch goed geformatteerd wordt, is er iets mis met je curly braces. Check ze. Negeer dat niet.
- Heb je teveel curly braces om mee te dealen? Heb je dan wel een functie geschreven die maar 1 ding doet? Keep your code simple! Check ook de FAQ, hoe krijgt ik minder spaghetti-code?

    [Mijn code is spaghetti-achtig geworden, hoe kan ik dit verbeteren?](@/hoe-voorkom-je-spaghetti-code.md)

- Lees de errors in je console goed!! Staat er X is not a function, terwijl jij heb wel gedefineerd hebt? Zijn je curly braces dan wel goed?
- In de console zie je ook op welke regel er een een error plaatsvindt, en waar er dus een curly brace ontbeekt.
- Wees blij dat je niet de programmeertaal 'Lisp' gebruikt: [voorbeeld](https://github.com/google/lisp-koans/blob/master/koans/hash-tables.lsp#L25)
