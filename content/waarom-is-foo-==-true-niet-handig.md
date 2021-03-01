+++
title = "Waarom is `foo == True` niet handig?"
extra.tags =[ "javascript", "python",]
created = "Apr 23, 2020 1:21 PM"
+++
# Waarom is `foo == True` niet handig? (booleans comparen)


## Python

Het is mogelijk om dit soort code te schrijven:

```python
# 🔴
foo = True
bar = False

if foo == True:
    print('foo == True')
else
    print('foo == False') 

if foo == True and bar == False:
    print('foo == True en bar == False')
else
    print('foo == False OF bar == True')
```

Maar dan ben je eigenlijk overbodig aan het comparen. Omdat `foo` en `bar` zelf al booleans zijn kun je ze ook direct gebruiken in statements die een boolean verwachten (zoals het `if` statement). Beter is dus:

```python
# ✅
foo = True
bar = False

if foo:
    print('foo == True')
else
    print('foo == False') 

if foo and not bar:
    print('foo == True en bar == False')
else
    print('foo == False OF bar == True')
```

## JavaScript

In JavaScript geldt hetzelfde:

Omslachtig:

```jsx
// 🛑
const foo = true;
const bar = false;

if (foo === true) {
  console.log('foo == true');
} else {
  console.log('foo == false');
}

if (foo === true && bar !== false) {
  console.log('foo == true en bar == false');
} else {
  console.log('foo == false OF bar == true');
}
```

Beter:

```jsx
// ✅
const foo = true;
const bar = false;

if (foo) {
  console.log('foo == true');
} else {
  console.log('foo == false');
}

if (foo && !bar) {
  console.log('foo == true en bar == false');
} else {
  console.log('foo == false OF bar == true');
}
```