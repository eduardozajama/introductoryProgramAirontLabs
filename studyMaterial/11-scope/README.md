# What is Scope?
Scope in JavaScript refers to the accessibility of variables, functions, and objects during runtime.

###mIn JavaScript, there are three types of scopes:

Global Scope
Functional Scope
Block Scope

## Global Scope:
Global scope is the outermost scope, a variable is in global scope if it’s declared outside of a block.
Window and document are global variables provided by the browser.
Variables inside the global scope can be accessed and altered in any other scope.

## Functional Scope:
Any variables or functions declared inside a function have local/functional scope, which means that they can be accessed within the function and not outside of it.

## Block Scope:
Block scope tells us that any variable declared inside a block {}, can be accessed only inside that block and cannot be accessed outside of it.
Block scope is related to variables declared using let and const only, var do not have block scope.

Block statements like if and switch conditions or for and while loops create a block-level scope.

A function creates a scope, so that (for example) a variable defined exclusively within the function cannot be accessed from outside the function or within other functions. For instance, the following is invalid:

```javascript

function exampleFunction() {
  const x = "declared inside function"; // x can only be used in exampleFunction
  console.log("Inside function");
  console.log(x);
}

console.log(x); // Causes error


```

## Hoisting:
When executing a JavaScript code, the JavaScript engine goes through two phases:

Parsing:
- JS engine moves all the variable declarations to the top of the page if the variable is global otherwise at top of the function if declared within a function.
Execution:
- JS engine assigns values to the variable and executes it.
So, hoisting is a mechanism that the JavaScript engine moves all the variables, functions declaration to the top of their scope, before the execution of the code. It allows functions and variables to be used in code before they are declared.

Take a look at the code below and guess what happens when we execute this:
``` javascript
console.log(data);
var data = 'hoist';
```
Every developer coming from any programming language will expect the output to be: ReferenceError: data is not defined, but instead, it will print undefined.

Why has this happened?

Just read the definition again about hoisting, JavaScript hoisted the variable declaration to the top of the scope, and this is what code looks like to the interpreter.
```javascript
var data;
console.log(data); // logs undefined
data = 'hoist';
```
Because of hoisting, we can use variables or functions before they are declared. Just remember hoisted variable is initialized with a value undefined.

Hoisting is not a term normatively defined in the ECMAScript specification. The spec does define a group of declarations as HoistableDeclaration, but this only includes function, function*, async function, and async function* declarations. Hoisting is often considered a feature of var declarations as well, although in a different way. In colloquial terms, any of the following behaviors may be regarded as hoisting:

- Being able to use a variable's value in its scope before the line it is declared. ("Value hoisting")
 - Being able to reference a variable in its scope before the line it is declared, without throwing a ReferenceError, but the value is always undefined. ("Declaration hoisting")
- The declaration of the variable causes behavior changes in its scope before the line in which it is declared.
The four function declarations above are hoisted with type 1 behavior; var declaration is hoisted with type 2 behavior; let, const, and class declarations (also collectively called lexical declarations) are hoisted with type 3 behavior.
>[More about Hoisting with examples](https://javascript.plainenglish.io/understanding-scoping-and-hoisting-in-javascript-with-examples-c51e5612d52e)

>[Hoisting in JS](https://www.digitalocean.com/community/tutorials/understanding-hoisting-in-javascript)

## Resources
>[Modzilla Dev](https://developer.mozilla.org/en-US/docs/Glossary/Scope)

>[Geeks for geeks](https://www.geeksforgeeks.org/strict-mode-javascript/)

>[digital ocean ](https://www.digitalocean.com/community/tutorials/understanding-hoisting-in-javascript)