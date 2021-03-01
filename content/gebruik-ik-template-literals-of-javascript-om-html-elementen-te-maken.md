+++
title = "Gebruik ik template literals of JavaScript om HTML elementen te maken?"
extra.tags =[ "dom", "javascript",]
created = "May 26, 2020 1:00 PM"
+++
# Gebruik ik template literals of JavaScript om HTML elementen te maken?


Als je in JavaScript nieuwe HTML elementen wil maken om ze aan de DOM toe te voegen kan dat op verschillende manieren:

1. template literals
2. document.createElement

Het is weer een stukje legacy van JavaScript en heeft te maken met de **backwards compatibility.** 

Template literals zijn een nieuwe frisse manier om complexe html element in JS snel te kunnen schrijven. In plaats van regel voor regel net JavaScript “document.createElement”, etc, etc, etc. Want dat voelt een beetje als overbodig en veel handmatig werk

Beide manieren zijn dus goed:
D**e JavaScript manier** is de 'oude' en 'robuuste' way-of-working. 
**Template literals** zijn de 'snelle' en 'nieuwe' manier. 

**Welke moet ik dan gebruiken?**
Het antwoord is: it depends. 
Voor beide methodes is wat te zeggen, maar wij raden template literals aan (tenzij je IE11 of ouder moet ondersteunen).
Waarom? Het leest wat lekkerder en het is minder code, en minder code = minder bugs.

> Lees hier een gehele blog van Wes Bos over waarom template literals fijn zijn: [https://wesbos.com/template-strings-html](https://wesbos.com/template-strings-html)

Template literals/strings kun je (nog) niet gebruiken in IE11 [https://caniuse.com/#feat=template-literals](https://caniuse.com/#feat=template-literals). 

**Zie ook**: [https://medium.com/@tforward/get-html-to-the-dom-fast-with-js-template-literals-insertadjacenthtml-24b8aa4e8807](https://medium.com/@tforward/get-html-to-the-dom-fast-with-js-template-literals-insertadjacenthtml-24b8aa4e8807)

Hieronder een voorbeeld om dit element te maken en vast te maken aan de ul.

```html
<li class='status'> 
  <p>Mijn Nieuwe Taak</p>
  <img src='trash-delete-icon.jpg' alt='delete icon'/>
</li>
```

```jsx
const list = document.querySelector('#list')
let newLi = document.createElement('li')
newLi.setAttribute('class', status)
let newImg = document.createElement('img')    
newImg.setAttribute('alt', 'delete icon');
newImg.setAttribute('src', 'trash-delete-icon.jpg');
let newText = document.createElement('p')
newText.innerHTML = task;
newLi.appendChild(newText);
newLi.appendChild(newImg);
list.appendChild(newLi).
```

**Alternatief met template literals:**

```jsx
const list = document.querySelector('#list');
const listItemRaw = `
  <li class='status'>
    <p>${task}</p>
    <img src='trash-delete-icon.jpg' alt='delete icon'/>
  </li>
`;
list.insertAdjacentHTML('beforeend', listItemRaw);
```