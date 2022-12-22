# 20. Prototypes
## What are prototypes?
Prototypes are the mechanism by which JavaScript objects inherit features from one another.you

As you know, you can create an object in JavaScript using an object constructor function. For example:
```javascript
// constructor function
function Person () {
    this.name = 'John',
    this.age = 23
}

// creating objects
const person1 = new Person();
const person2 = new Person();
```

In the above example, function Person() is an object constructor function. We have created two objects person1 and person2 from it.

## JavaScript Prototype
In JavaScript, every function and object has a property named prototype by default. For example,
```javascript
function Person () {
    this.name = 'John',
    this.age = 23
}

const person = new Person();

// checking the prototype value
console.log(Person.prototype); // { ... }
```

In the above example, we are trying to access the prototype property of a Person constructor function.

Since the prototype property has no value at the moment, it shows an empty object { ... }.

## Resources
>[Geeks for geeks ](https://www.geeksforgeeks.org/prototype-in-javascript/)

>[JS tutorial](https://www.tutorialsteacher.com/javascript/prototype-in-javascript)

>[JS Prototype](https://www.tutorialsteacher.com/javascript/prototype-in-javascript)

>[Mozilla dev](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object_prototypes)

