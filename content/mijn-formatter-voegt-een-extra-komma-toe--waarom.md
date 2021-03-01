+++
title = "Mijn formatter voegt een extra komma toe, waarom?"
extra.tags =[ "javascript", "python",]
created = "Apr 23, 2020 12:26 PM"
+++
# Mijn formatter voegt een extra komma toe, waarom?


Als je een formatter gebruikt voor je code kan het zijn dat deze soms een extra komma aan het einde van bepaalde regels zet. Voorbeeld (in Python)

```python
foo = [
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'wereld', # 👈
]
```

Zelfde voorbeeld in JavaScript:

```python
const foo = [
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'hallo',
    'hallo',
];
```

Die komma is technisch niet nodig, en mag wel. Het toevoegen van die komma heeft een paar voordelen:

- je kan de items in deze list makkelijker veranderen van volgorde
- je diffs worden cleaner
- als je een nieuw item toevoegt aan je list kan je de komma niet vergeten (want hij staat er al)

Lees meer:

[Why you should enforce Dangling Commas for Multiline Statements](https://medium.com/@nikgraf/why-you-should-enforce-dangling-commas-for-multiline-statements-d034c98e36f8)