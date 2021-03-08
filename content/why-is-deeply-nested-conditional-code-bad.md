+++
title = "Why is deeply nested conditional code bad?"
extra.tags =[ "javascript", "python", "principles",]
created = "Dec 15, 2020 2:35 PM"
+++
# Why is deeply nested (conditional) code bad?


We say code is 'deeply nested' when your program can take a lot of different paths in a code block. This can easily happen when you have a lot of nested conditional statements. But it can also happen with other kinds of code.

An example in JavaScript:

```js
const startCar = person => {
    if (person.age >= 18) {
        if (hasDriversLicense(person)) {
            if (hasCar(person)) {
                if (getFuelInLiters(getCar(person)) > 5) {
                    let car = getCar(person);
                    car.start();
                    car.drive();
                }
            }
        }
    }
};
```

Another example:

```js
// Check if item is available for sale
if (item.IsAvailableForSale)
{
    // Check if payment has been made
    if (payment.IsPaymentMade)
    {
        // Check if amount paid is sufficient
        if (payment.Amount >= item.Price)   
        {
            // Check if the item has stock in store
            if (store.HasStock(item.Id))        
            {
                // Place order from store
            }
            else
            {
                // Check if the item has stock in warehouse
                if (warehouse.HasStock(item.Id))    
                {
                    // Place order from warehouse
                }
                else
                {
                    // Out of stock
                }
            }
        }
        else
        {
            // Insufficient funds
        }
    }
    else 
    {
        // Ask for payment
    }
}
else
{
    // Product is not available
}
```

Deeply nested code is problematic for a number of reasons:

**Understanding code is harder**

This kind of code is hard to understand. If you go into a deeply nested code structure you need to remember the decisions that your program makes each step you go down. Keeping more than a couple of things in your head makes it harder to do other stuff.

**Making mistakes is easy**

In deeply nested code it's very easy to miss that certain code paths will lead to an unwanted result. Or in other words: it's hard to see that each branch in your code has a good result.

**Visually hard**

Most languages indent when they nest code like this. If your code is deeply nested you'll soon have to scroll sideways to see all of your code. This is uncomfortable for most people.

Matching an `if` to an `else` in a deeply nested code block is hard if there are a lot of nested code lines in between. Your editor can help with this by adding vertical lines, giving your parentheses similar colors or folding lines of code, but these are all bandaids for the bigger problem.

## How do I get rid of deeply nested conditional code?

That's a great question, I'm glad you asked.

Sometimes it can be hard to get rid of deeply nested conditional code simply because the 'domain' in which you're working is complicated. However here are a few tactics:

**Early returns (aka 'guard clauses')**

When you're inside of a function (and most code is written in functions) it's often a good idea to pre-check certain conditions before going deeper into the function. If those conditions are not met we can jump out of the function early.

For example:

```js
// Deeply nested
const startCar = person => {
    if (person.age >= 18) {
        if (hasDriversLicense(person)) {
            if (hasCar(person)) {
                if (getFuelInLiters(getCar(person)) > 5) {
                    let car = getCar(person);
                    car.start();
                    car.drive();
                }
            }
        }
    }
};

// Early returns
const startCar = person => {
    if (person.age < 18) return;
    if (!hasDriversLicense(person)) return;
    if (!hasCar(person)) return;
    if (getFuelInLiters(getCar(person)) <= 5) return;

    let car = getCar(person);
    car.start();
    car.drive();
};
```

Some people would argue that having a lot early returns in your code is itself problematic, however that's a whole other discussion that we'll not discuss now.

**Inlining conditionals**

Another thing you can do is to gather a bunch of conditionals together, maybe even give them a temporary variable.

```js
// Deeply nested
const startCar = person => {
    if (person.age >= 18) {
        if (hasDriversLicense(person)) {
            if (hasCar(person)) {
                if (getFuelInLiters(getCar(person)) > 5) {
                    let car = getCar(person);
                    car.start();
                    car.drive();
                }
            }
        }
    }
};

// Inlining conditionals + temporary variables
const startCar = person => {
    const isAdult = person.age >= 18;
    const hasLicense = hasDriversLicense(person);
    const carHasEnoughFuel = getFuelInLiters(getCar(person)) > 5;

    if (isAdult && hasLicense && hasCar(person) && carHasEnoughFuel) {
        let car = getCar(person);
        car.start();
        car.drive();
    }
};
```

**Use 'helper functions'**

We can make deeply nested code simpler by using functions to divide up our conditionals into different functions.

```js
// Deeply nested
const startCar = person => {
    if (person.age >= 18) {
        if (hasDriversLicense(person)) {
            if (hasCar(person)) {
                if (getFuelInLiters(getCar(person)) > 5) {
                    let car = getCar(person);
                    car.start();
                    car.drive();
                }
            }
        }
    }
};

// Use helper functions
const personCanDrive = person => person.age >= 18 && hasDriversLicense(person);
const carCanDrive = car => getFuelInLiters(car) > 5;

const startCar = person => {
    let car = getCar(person);
    const carHasEnoughFuel = carCanDrive(car);

    if (personCanDrive(person) && hasCar(person) && carHasEnoughFuel) {
        car.start();
        car.drive();
    }
};
```

**Other strategies**

- If your language supports `switch` statements using them can potentially help
- If your language supports `else if` statements using them can potentially help

## Further reading

[Computer Programming/Coding Style/Minimize nesting](https://en.wikibooks.org/wiki/Computer_Programming/Coding_Style/Minimize_nesting)

[Flattening Arrow Code](https://blog.codinghorror.com/flattening-arrow-code/)