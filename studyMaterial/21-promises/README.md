# 21. Promises
Understanding JavaScript Promises
By definition, a promise is an object that encapsulates the result of an asynchronous operation.

A promise object has a state that can be one of the following:

* Pending
* Fulfilled with a value
* Rejected for a reason

In the beginning, the state of a promise is pending, indicating that the asynchronous operation is in progress. Depending on the result of the asynchronous operation, the state changes to either fulfilled or rejected.

The fulfilled state indicates that the asynchronous operation was completed successfully:
The rejected state indicates that the asynchronous operation failed.

## Creating a promise
To create a promise object, you use the Promise() constructor:
```javascript
const promise = new Promise((resolve, reject) => {
  // contain an operation
  // ...

  // return the state
  if (success) {
    resolve(value);
  } else {
    reject(error);
  }
});
```
The promise constructor accepts a callback function that typically performs an asynchronous operation. This function is often referred to as an executor.

In turn, the executor accepts two callback functions with the name resolve and reject.

Note that the callback functions passed into the executor are resolve and reject by convention only.

If the asynchronous operation completes successfully, the executor will call the resolve() function to change the state of the promise from pending to fulfilled with a value.

In case of an error, the executor will call the reject() function to change the state of the promise from pending to rejected with the error reason.

Once a promise reaches either fulfilled or rejected state, it stays in that state and can’t go to another state.

In other words, a promise cannot go from the fulfilled state to the rejected state and vice versa. Also, it cannot go back from the fulfilled or rejected state to the pending state.

Once a new Promise object is created, its state is pending. If a promise reaches fulfilled or rejected state, it is resolved.

Note that you will rarely create promise objects in practice. Instead, you will consume promises provided by libraries.

## Resources
>[Mozila Dev](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Promises)

>[JS info](https://javascript.info/promise-basics)
>[JS tutorial](https://www.javascripttutorial.net/es6/javascript-promises/)

