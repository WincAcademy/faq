+++
title = "Mijn link werkt op mijn computer maar niet online, waarom?"
extra.tags =[ "html",]
created = "Mar 5, 2020 1:25 PM"
+++
# HTML: Mijn link werkt op mijn computer maar niet online, waarom?
 Waarschijnlijk heb je dan het gehele 'pad' op je computer in je <a> gezet als href. In plaats van een 'relatief pad'. Maak je href een relatief pad.

In plaats van: 

<a href='/Users/marjoleintrompwerk/VSCODE/WincAcademy/Mini Course/Opdracht_002/contact.html'>contact</a>

.. maak je een relatief pad:
<a href='contact.html'>contact</a>