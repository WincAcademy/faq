+++
title = "What are the best practices in the render function of a React component?"
extra.tags =[ "react",]
created = "Jan 11, 2021 5:48 PM"
+++
# What are the best practices in the render function of a React component?


You should try to keep your render functions simple and clean.

Don't

- define functions inside of the render method (they'll be defined again and again, making your code less fast)
- put a lot of logic in your render function, some conditionals are fine, but do complex data transformations outside of the render function to make it easier to test