+++
title = "Ik maak een variable die ik maar één keer gebruik, kan dat handiger?"
extra.tags =[ "javascript",]
created = "Feb 10, 2020 2:56 PM"
+++
# Ik maak een variable die ik maar één keer gebruik, kan dat handiger?
Soms maak je een variabele aan die je maar één keer gebruikt. Daar kan je een goeie reden voor hebben, maar vaak kan je in JavaScript dat dingen in één keer doen.

Voorbeeld:

```js
// Langer
const liMenu = document.querySelector('.colormenu');
liMenu.addEventListener('click', function() {
  toggle();
});

// Korter
document.querySelector('.colormenu').addEventListener('click', function() {
  toggle();
});
```