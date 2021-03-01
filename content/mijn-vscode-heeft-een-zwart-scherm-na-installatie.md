+++
title = "Mijn VSCode heeft een zwart scherm na installatie"
extra.tags =[ "praktisch",]
created = "Mar 19, 2020 10:47 AM"
+++
# Mijn VSCode heeft een zwart scherm na installatie
VSCode draait niet standaard goed op Windows 7.

Je hebt 2 opties: windows 10 installeren of de GPU van VSCode uitzetten. 

VS Code is blank?
The Electron shell used by Visual Studio Code has trouble with some GPU (graphics processing unit) hardware acceleration. If VS Code is displaying a blank (empty) main window, you can try disabling GPU acceleration when launching VS Code by adding the Electron --disable-gpu command-line switch.
code --disable-gpu

Bron: https://code.visualstudio.com/Docs/supporting/faq#_vs-code-main-window-is-blank