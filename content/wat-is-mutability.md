+++
title = "Wat is mutability?"
answer = "Zie pagina"
extra.tags =[ "javascript",]
created = "Feb 12, 2020 11:48 AM"
+++
# Wat is mutability?


Met een variabele in JavaScript kun je van alles doen. En het 'iets doen' noemen we ook wel 'operaties'.

1 je kan de waarde gebruiken:
`let result = 3 + a;`

2 je kan een property van de variabele lezen:
`let numFilms = films.length;`

3 je kan een methode (functie) die aan een variabele vastzit aanroepen:
`films.sort();`

4 je kan de variabele als argument aan een functie geven:
`let result = getFilmsAfter2000(films);`

Sommige van deze 'operaties' (dingen die je doet met een variabele) *veranderen* de variabele. In het Engels 'mutate'. Met andere woorden: als de waarde van een variable *anders* kan zijn **voor** en **na** de operatie dan was de operatie 'mutable'. Als de waarde van een variable altijd het zelfde is **voor** en **na** de operatie dan was de operatie 'immutable'. 

Voorbeelden:

```js
let a = 5;
let movies = ['Die Hard', 'Robocop', 'Back to the Future'];

// Immutable
let result = 8 + a;

// Immutable
let numMovies = movies.length;

// Mutable
movies.sort();

// Mutable
let lastMovie = movies.pop();

// Mutable
movies.push('Aliens');

// Immutable
let allMovies = movies.join(', ');

// Immutable
const movieIsNew = function (movie) {
  // only return true if movie is made after 2000
  return true;
};
let newMovies = movies.filter(movieIsNew);
```

Met JavaScript maken we zelf ook operaties, namelijk functies 🎉
Die operaties (functies) die we zelf maken kunnen *ook* mutable of immutable zijn. Het ligt er dan aan wat we in de functie doen met die variabele.
* Muteren we de variabele in de functie?  ➡️ Dan is de functie mutable. 
* Muteren we de variabele niet? ➡️ Dan is de functie immutable.

In je opleiding leer je welke functies al dan niet muteren.
