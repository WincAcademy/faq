+++
title = "Why would I use a function component instead of a class component?"
extra.tags =[ "react",]
created = "Jan 11, 2021 2:21 PM"
+++
# Why would I use a function component instead of a class component?


In React you can create components with classes or with functions.

## Without React Hooks

When you use a class component you have to write a bit more code but you get access to a lot more functionality.

However: if you don't need this functionality because your component is relatively simple it's better to just write a function. This both shows that your component is simple (to others that read your code) and it saves you time because you have to type less.

You can always convert a class component to a function component or back.

## With React Hooks

If you use React Hooks you can still write function components, but you can get pretty much all the functionality that class components also have.

React Hooks is the future, but there's still a lot of class components that you will see.

Some people prefer using function components and React Hooks over class component.