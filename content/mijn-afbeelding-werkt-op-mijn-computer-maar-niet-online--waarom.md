+++
title = "Mijn afbeelding werkt op mijn computer maar niet online, waarom?"
extra.tags =[ "html",]
created = "Feb 20, 2020 11:56 AM"
+++
# Mijn afbeelding werkt op mijn computer maar niet online, waarom?

Waarschijnlijk heb je dan het gehele 'pad' op je computer in je img gezet als src. In plaats van een 'relatief pad'. Maak je src een relatief pad.

In plaats van: '/Users/marjoleintrompwerk/VSCODE/WincAcademy/Mini Course/Opdracht_002/winc-round.png' 

Zet je de afbeelding in de juiste map en maak je een relatief pad, namelijk van de HTML file, naar de afbeelding. In de HTML file: 
Maak je: 'winc-round.png'