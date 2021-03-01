+++
title = "React how to give a unique id to each child element?"
extra.tags =[ "react",]
created = "Dec 22, 2020 2:47 PM"
+++
# React: how to give a unique id to each child element?


When you want to render a list of items in React you need to provide each item a unique key, the why is explained here.

[Lists and Keys - React](https://reactjs.org/docs/lists-and-keys.html)

So what key should you use?

## Don't use the index

It might be tempting to use the index of the item in the array of items you're rendering, but that will lead to certain issues.

Read this article for more info:

[Index as a key is an anti-pattern](https://medium.com/@robinpokorny/index-as-a-key-is-an-anti-pattern-e0349aece318)

Or see this video:

[ReactJS Tutorial - 19 - Index as Key Anti-pattern](https://youtu.be/xlPxnc5uUPQ)

## Best practice

If you *can* generate a unique value from the thing you're displaying you can do that. If you cannot you should use a library that can generate unique id's. For example:

[nanoid](https://www.npmjs.com/package/nanoid)