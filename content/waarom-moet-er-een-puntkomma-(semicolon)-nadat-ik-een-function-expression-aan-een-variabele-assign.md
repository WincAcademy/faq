+++
title = "Waarom moet er een puntkomma (semicolon) nadat ik een function expression aan een variabele assign?"
extra.tags =[ "javascript",]
created = "Feb 17, 2020 1:49 PM"
+++
# Waarom moet er een puntkomma (semicolon) nadat ik een function expression aan een variabele assign?


Als je iets aan een variabele assigned doe je dit, je maakt een waarde (een expression) en die *assign* je aan een variabele.

`let a = 3;`

`const b = 5;`

Als je een functie maakt en die aan een variabele assigned doe je precies hetzelfde, je maakt een waarde (de function expression) en die *assign* je aan een variabele. Daarom wil je daarna ook een `;`.

```jsx
const wordIsLongerThan5Chars = word => word.length > 5;

const isOldXmenMovie = movie => {
    return (movie.year < 2000 && movie.title.includes('X-men'));
}; // Hiero dus!
```