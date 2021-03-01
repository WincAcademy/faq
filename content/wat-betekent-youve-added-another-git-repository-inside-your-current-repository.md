+++
title = "Wat betekent 'you've added another git repository inside your current repository'?"
extra.tags =[ "git",]
created = "Feb 10, 2020 4:49 PM"
+++
# Wat betekent 'you've added another git repository inside your current repository'?
Een git repository is eigenlijk gewoon een directory. Daar kun je van alles in doen.

Je kan daar zelfs een andere repository in clonen of kopieren. Git raakt daar wel erg van in de waar en waarschuwt je dan.

Dus: doe dat vooral niet :-)

Tijdens het toevoegen van je bestanden in versiebeheer met `git add <path>` krijg je de volgende foutmelding te zien: 

> You've added another git repository inside your current repository

Dit houdt in dat er al een repository bestaat binnen je huidige repository. Waarschijnlijk heb je een repository aangemaakt in één van de onderliggende folders met het commando `git init` . Git raakt hierdoor in de war, aangezien het niet mogelijk is een om repository binnen een repository in versiebeheer te hebben (dit is technisch wel mogelijk met [Git Submodules](https://git-scm.com/book/nl/v2/Git-Tools-Submodules), maar dat is best ingewikkeld).

Denk je dat dit bij jou het geval is? Check dan of er meer dan één `.git` directory in je repository zit. Als je er meer dan één hebt: foute boel. Je wil per repository maar één zo'n directory hebben. Gooi de .git directory/directories weg die in subfolders zitten.