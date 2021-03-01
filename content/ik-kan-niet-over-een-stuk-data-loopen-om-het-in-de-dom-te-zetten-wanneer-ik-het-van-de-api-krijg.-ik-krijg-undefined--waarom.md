+++
title = "Ik kan niet over een stuk data loopen om het in de DOM te zetten wanneer ik het van de API krijg. Ik krijg undefined, waarom?"
extra.tags =[ "api", "javascript", "async",]
created = "Dec 19, 2019 1:12 PM"
+++
# Ik kan niet over een stuk data loopen om het in de DOM te zetten wanneer ik het van de API krijg. Ik krijg undefined, waarom? (Werken met grote stukken data van een API - Objects vs Arrays)

ook `undefined`, omdat de array `data.genres`, geen property `name` heeft.

## Een voorbeeld:

```jsx
data { 
 genres: [
        {id: Blah, name: 'Action'}, 
        {id: Hoi, name: 'Science Fiction'}
       ]
}
```

**data.forEach() 👉 levert `undefined` op. Waarom?** 

**Hoe kom je bij de genres?**

Die kun je dus heel simpel aanspreken: `data.genres`. 

`**data.genres` is wél een array 🎉.**

Namelijk: `[{id: Blah, name: 'Action'}, {id: Hoi, name: 'Science Fiction'} ]`
Over een array kun je uiteraard wél loopen. 

**Nog een begrip vraag: Wat levert `data.genres.name` op?** 


**Wat lever `data.genres[0].name` op?** 

Antwoord De `name` van het eerste `genre`.