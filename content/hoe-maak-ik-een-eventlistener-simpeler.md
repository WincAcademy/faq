+++
title = "Hoe maak ik een eventListener simpeler?"
extra.tags =[]
created = "Apr 1, 2020 2:50 PM"
+++
# Hoe maak ik een eventListener simpeler?


Als je zo een event listener aan een element toevoegt:

```jsx
document.getElementById('nieuwste').addEventListener('change', function () {
    filterLatestMovies()
});
```

Dan doet de functie die je geeft aan `addEventListener` niet zoveel, het is dan een doorgeefluik.

Schrijf in plaats daarvan dan dit:

```jsx
document.getElementById('nieuwste').addEventListener('change', filterLatestMovies);
```