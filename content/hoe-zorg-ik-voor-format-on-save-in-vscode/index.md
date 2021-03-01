+++
title = "Hoe zorg ik voor 'Format On Save' in VSCode?"
answer = "Check het uitgebreide antwoord"
extra.tags =[ "praktisch",]
created = "Feb 20, 2020 1:18 PM"
+++
# Hoe zorg ik voor 'Format On Save' in VSCode?


## Formatten

Met formatten bedoelen we: het juist gebruiken van spaties, tabs en enters. 

- Onjuist voorbeeld

    ```jsx
    <!-- Onjuist: -->
    <main>
    					      <ul>
    								<li> Boter </li>
    								                 <li> Kaas </li>
    								<li> Eieren </li>

    </ul>

        </main>
    ```

- Juist voorbeeld

    ```jsx
    <main>
      <ul>
        <li>Boter</li>
        <li>Kaas</li>
        <li>Eieren</li>
      </ul>
    </main>
    ```

Let op: voor je computer maakt dit niet uit. Jouw browser is helemaal tevreden met het onjuiste voorbeeld en zal het ook netjes aan je presenteren. Echter is het voor ons mensen veel beter lezen en maak je minder fouten als je op de juiste manier je files formatteert. 

Gelukkig hoef je dat niet handmatig te doen ⭐

VSCode heeft een hele handige instelling:

Code > Preferences > Settings > zoek naar 'format on save' > vink aan

![format-on-save.png](@/format-on-save.png)