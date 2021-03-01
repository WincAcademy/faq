+++
title = "origin does not appear to be a git repository, Could not read from remote repository."
extra.tags =[ "git",]
created = "Feb 10, 2020 12:08 PM"
+++
# 'origin' does not appear to be a git repository, Could not read from remote repository.


Je krijgt deze error omdat je geen remote hebt toegevoegd aan je lokale git repository. Oftwel git vertelt je met deze error 'joe ik heb geen idee waar ik geen gepushed moet worden' 

Stap 1: Check of het inderdaad klopt dat je geen remote hebt met `git remote -v` 
Je verwacht dan geen uitkomst. Krijg je wel een uitkomst? Dan is er iets anders aan de hand. 
Typo wellicht?

Stap 2: voeg jouw remote toe aan je lokale git repository (een remote is het 'adres' van je online git repository op GitHub, waar jouw code naartoe gepushed moet worden) 
Lees: [https://help.github.com/en/github/using-git/adding-a-remote](https://help.github.com/en/github/using-git/adding-a-remote) 

Mijn remote? Ik heb nog geen remote? 

Dan heb je de stap gemist om een repository aan te maken op GitHub, en daar de stappen te volgen. 

Hoe ziet een remote eruit?

Bijvoorbeeld zo: [`git@github.com](@/mailto:git@github.com):WincAcademy/mini-course-opdrachten-oplossingen.git`