+++
title = "Wat is moderne JavaScript syntax?"
extra.tags =[ "javascript",]
created = "Jun 4, 2020 7:43 PM"
+++
# Wat is moderne JavaScript syntax?


JavaScript is een taal die al een tijdje bestaat. In de afgelopen 10 jaar zijn er een aantal toevoegingen aan de taal gedaan die het mogelijk maken om je code beter te maken, minder foutgevoelig of simpelweg korter. Hieronder een kort overzichtje van wat je beter wel en niet kan doen.

### Variabelen aanmaken

Oud:

```jsx
var a = 1;
```

Nieuw:

```jsx
const a = 1;
// of als de waarde moet kunnen veranderen: let
let b = 2;
```

### Functies

Oud:

```jsx
function foo () {
  return 4;
}
```

Nieuw:

```jsx
const foo = () => 4;
```

### Strings aan elkaar plakken

Oud:

```jsx
'Hello ' + name;
```

Nieuw:

```jsx
`Hello ${name}`
```

### Loops

Oud:

```jsx
const qux = [1,2,3,4];
for (var i = 0; i < qux.length; i++){
  console.log(qux[i]);
}
```

Nieuw:

```jsx
const qux = [1,2,3,4];
qux.forEach(console.log);
```

Als je loops gebruikt om een nieuw array te maken: gebruik `array.map`.

Als je loops gebruikt om elementen te filteren: gebruik `array.filter`.

### Waardes uit een object pakken (destructuring)

Voorbeeld gekopieerd van [Mosh](https://programmingwithmosh.com/javascript/essential-modern-javascript-features/).

Oud:

```jsx
const person = { 
   name: 'Mosh', 
   address: {
      billing: { 
         street: '123 Flinders st',
         city: 'Melbourne',
         state: 'Victoria'
      }
   }
};
const street = person.address.billing.street;
const city = person.address.billing.city;
const state = person.address.billing.state;
```

Nieuw:

```jsx
const person = { 
   name: 'Mosh', 
   address: {
      billing: { 
         street: '123 Flinders st',
         city: 'Melbourne',
         state: 'Victoria'
      }
   }
};
const { street, city, state } = person.address.billing;
```