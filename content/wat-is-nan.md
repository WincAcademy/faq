+++
title = "Wat is NaN?"
extra.tags =[ "javascript",]
created = "Feb 12, 2020 4:35 PM"
+++
# Wat is NaN?
Zie https://javascript.info/types

`NaN` is een standaard JavaScript eigenschap van het type `Number`  en staat voor '**Not-A-Number**'.

**Hoe controleer ik of een waarde gelijk is aan** `NaN` **?**

```js
const waarde = NaN;

if (Number.isNan(waarde)) {
    console.log('De waarde is NaN');
}
```