# 22. ASYNC, AWAIT

## What is Synchronous Programming?
Synchronous programming includes the sequential execution of functions and processes. If a particular function needs a resource, execution stops until the currently executing function fetches the resource and finishes its process.
Although this ensures that the execution is error-free, it’s time-consuming and doesn’t use the system to its full potential. Asynchronous programming solves these issues.

## What is Asynchronous Programming?
Asynchronous programming, on the other hand, ensures that the execution does not stop if a function is performing other operations. Instead, the execution continues normally until the function is called back again. To facilitate this, concepts like Callbacks, Promises, and Async/await are used.

## async/ await
ES2017 introduced the async/await keywords that build on top of promises, allowing you to write asynchronous code that looks more like synchronous code and is more readable. Technically speaking, the async / await is syntactic sugar for promises.

## The async keyword
The async keyword allows you to define a function that handles asynchronous operations.

To define an async function, you place the async keyword in front of the function keyword as follows:
```javascript
async function sayHi() {
    return 'Hi';
}
```

Asynchronous functions execute asynchronously via the event loop. It always returns a Promise. 

In this example, because the sayHi() function returns a Promise, you can consume it, like this:
```
sayHi().then(console.log);
```

You can also explicitly return a Promise from the sayHi() function as shown in the following code:
```javascript
async function sayHi() {
    return Promise.resolve('Hi');
}

```
The effect is the same.

Besides the regular functions, you can use the async keyword in the function expressions:
```javascript
let sayHi = async function () {
    return 'Hi';
}
```

arrow functions:
```javascript
let sayHi = async () => 'Hi'; 
```
and methods of classes:
```javascript
class Greeter {
    async sayHi() {
        return 'Hi';
    }
}
```
## The await keyword
You use the await keyword to wait for a Promise to settle either in resolved or rejected state. And you can use the await keyword only inside an async function:
```javascript
async function display() {
    let result = await sayHi();
    console.log(result);
}
```

In this example, the await keyword instructs the JavaScript engine to wait for the sayHi() function to complete before displaying the message.

Note that if you use the await operator outside of an async function, you will get an error

## Error Handling
Handling errors in async functions is very easy. Promises have the .catch() method for handling rejected promises, and since async functions just return a promise, you can simply call the function, and append a .catch() method to the end.
```javascript
asyncFunctionCall().catch(err => {
  console.error(err)
});
```

But there is another way: the mighty try/catch block! If you want to handle the error directly inside the async function, you can use try/catch just like you would inside synchronous code.
```javascipt
async function getPersonsInfo(name) {
  try {
    const people = await server.getPeople();
    const person = people.find(person => { return person.name === name });
    return person;
  } catch (error) {
    // Handle the error any way you'd like
  }
}
```
Doing this can look messy, but it is a very easy way to handle errors without appending .catch() after your function calls. How you handle the errors is up to you, and which method you use should be determined by how your code was written. You will get a feel for what needs to be done over time. The assignments will also help you understand how to handle your errors.

## Resources

https://www.javascripttutorial.net/es-next/javascript-async-await/
https://www.geeksforgeeks.org/async-await-function-in-javascript/
https://javascript.info/async-await
https://www.programiz.com/javascript/async-await
https://www.simplilearn.com/tutorials/javascript-tutorial/javascript-async-await





