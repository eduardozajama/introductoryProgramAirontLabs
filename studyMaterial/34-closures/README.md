# 34. Closures
## What are Closures?
A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function's scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.

#### Remember:

The function scope is created for a function call, not for the function itself
Every function call creates a new scope
When the function has finished the execution, the scope is usually destroyed. A simple example of such function is this:
```javascript
function buildName(name) { 
    var greeting = "Hello, " + name; 
    return greeting;
}
```

It doesn’t get more simple than that. The function buildName() declares a local variable greeting and returns it. Every function call creates a new scope with a new local variable and. After the function is done executing, we have no way to refer to that scope again, so it’s garbage collected.
But how about when we have a link to that scope? Let’s look at the next function:
```javascript
function buildName(name) { 
    var greeting = "Hello, " + name + "!"; 
    var sayName = function() {
        var welcome = greeting + " Welcome!";
        console.log(greeting); 
    };
    return sayName; 
}

var sayMyName = buildName("John");
sayMyName();  // Hello, John. Welcome!
sayMyName();  // Hello, John. Welcome!
sayMyName();  // Hello, John. Welcome!
```

The function sayName() from this example is a closure.

A closure is a function which has access to the variable from another function’s scope. This is accomplished by creating a function inside a function. Of course, the outer function does not have access to the inner scope.

The sayName() function has it’s own local scope (with variable welcome) and has also access to the outer (enclosing) function’s scope. It this case, the variable greeting from buildName().

After the execution of buildName is done, the scope is not destroyed in this case. The sayMyName() function still has access to it, so it won’t be garbage collected. However, there is not other way of accessing data from the outer scope except the closure.

This is the big gotcha of the entire concept. The closure serve as the gateway between the global context and the outer scope. I cannot access directly variables from the outer scope if the closure is not allowing it. This way, I can protect the variables from the outer scope. They are – by all means – private and the closure can serve as a getter or setter for them.

## Resources
https://www.javatpoint.com/javascript-closures
https://www.geeksforgeeks.org/what-is-the-practical-use-for-a-closure-in-javascript/
https://www.javascripttutorial.net/javascript-closure/
https://www.codingame.com/playgrounds/6516/closures-in-javascript-for-beginners







