+++
title = "How do I create a 'divide algorithm'?"
extra.tags =[ "javascript", "algorithms",]
created = "Jan 25, 2021 6:11 PM"
+++
# How do I create a 'divide algorithm'?


```jsx
/*
We've got a series of objects. We want to divide or categorize those objects
into separate 'buckets'. We want to do that on the basis of an attribute.

Basically this algorithm that we're writing has two steps:

1. make a list of buckets
2. divide the items over the buckets

To be able to do this we need certain functionality:

- read attribute X from an object
- do we have a bucket for X?
- get the bucket for X
- create the bucket for X
- add an item to a bucket

Some of this functionality is so simple we don't want to write a function for
it. For others we do want to write a function.

So let's implement this so we can divide these animals into their continents.
*/

const animals = [{
        name: 'monkey',
        food: 'bananas',
        weight: 60,
        max_age: 30,
        continent: 'Africa',
        flies: false,
        nocturnal: false,
    },
    {
        name: 'rhino',
        food: 'grass',
        weight: 800,
        max_age: 40,
        continent: 'Africa',
        flies: false,
        nocturnal: false,
    },
    {
        name: 'bat',
        food: 'insects',
        weight: 1,
        max_age: 5,
        continent: 'Asia',
        flies: true,
        nocturnal: true,
    },
    {
        name: 'tapir',
        food: 'insects',
        weight: 20,
        max_age: 80,
        continent: 'South-America',
        flies: false,
        nocturnal: true,
    },
    {
        name: 'lion',
        food: 'meat',
        weight: 200,
        max_age: 50,
        continent: 'Africa',
        flies: false,
        nocturnal: true,
    },
    {
        name: 'cow',
        food: 'grass',
        weight: 600,
        max_age: 60,
        continent: 'Europe',
        flies: false,
        nocturnal: false,
    },
    {
        name: 'moose',
        food: 'grass',
        weight: 800,
        max_age: 50,
        continent: 'Europe',
        flies: false,
        nocturnal: false,
    },
    {
        name: 'house cat',
        food: 'meat',
        weight: 20,
        max_age: 15,
        continent: 'Europe',
        flies: false,
        nocturnal: false,
    },
];

const bucketForValueExists = (buckets, attributeValue) =>
    attributeValue in buckets;

const addBucket = (buckets, attributeValue) => {
    // Add an empty array under 'Africa' so we can add animals to this array
    // later on
    buckets[attributeValue] = [];
    return buckets;
};

/*
So now we have the functions that will help us create and add to buckets. Let's
start using them.
*/

// Create buckets
let buckets = {};
const attribute = 'continent'; // We want to divide based on continent
animals.forEach(animal => {
    const attributeValue = animal[attribute]; // 'Africa' for example
    if (!bucketForValueExists(buckets, attributeValue)) {
        buckets = addBucket(buckets, attributeValue);
    }
});

// Now let's put the animals into the bucket they belong
animals.forEach(animal => {
    const attributeValue = animal[attribute]; // 'Africa' for example
    buckets[attributeValue].push(animal); // Find the right bucket and add the animal to the array of that bucket
});

console.log(buckets);

// We could make this a lot more compact and iterate only once, but that makes
// it harder to read.
const divided = animals.reduce((buckets, current) => {
    const attributeValue = current.continent;
    if (!(attributeValue in buckets)) buckets[attributeValue] = [];
    buckets[attributeValue].push(current);
    return buckets;
}, {});
console.log(divided);
```