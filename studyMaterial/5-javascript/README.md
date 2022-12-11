# 5. JavaScript 
## What is JavaScript?
JavaScript is a programming language initially designed to interact with elements of web pages. In web browsers, JavaScript consists of three main parts:
ECMAScript provides the core functionality.
The Document Object Model (DOM) provides interfaces for interacting with elements on web pages
The Browser Object Model (BOM) provides the browser API for interacting with the web browser.
JavaScript allows you to add interactivity to a web page. Typically, you use JavaScript with HTML and CSS to enhance a web page’s functionality, such as validating forms, creating interactive maps, and displaying animated charts.
When a web page is loaded, i.e., after HTML and CSS have been downloaded, the JavaScript engine in the web browser executes the JavaScript code. The JavaScript code then modifies the HTML and CSS to update the user interface dynamically.
The JavaScript engine is a program that executes JavaScript code. In the beginning, JavaScript engines were implemented as interpreters.
However, modern JavaScript engines are typically implemented as just-in-time compilers that compile JavaScript code to bytecode for improved performance.




## How To Use Javascript

To use javascript in your website project, there are two main methods;
#### - INTERNAL JAVASCRIPT

Here, the script codes are presented in the same HTML file of which it would be used. The codes are displayed in-between the open ``` <script>``` and close ```</script>``` script tags. E.g
 
 ```javascript

<!-- index.html file -->

<!DOCTYPE html>
<html>
  <head>
    <title>Javascript Syntax and Basic Constructs</title>
  </head>
  <body>
    <h1>Hello</h1>

    <!-- Javascript area -->
    <script>
      console.log('Hey, Javascript!!');
    </script>
  </body>
</html>
```

``` console.log ```might not be understood, but we are going to see that later.
 
 
 
 
 
 
 
 
#### - EXTERNAL JAVASCRIPT

Here, the script codes are placed in another file and are simply referenced in the HTML file of which it is to be used.
For our program above, we could simply have a different file for it;
 ```javascript

// script.js
console.log('Hey, Javascript!!');

```

In our index.html, we could simply replace the Javascript area with 

```javascript 
<script src='script.js'></script> 
```
 
The src attribute means source which contains the location of the javascript file we are trying to reference.
 
#### Advantages of External Javascript

It separates your HTML elements and codes
It makes your HTML files and javascript files easier to read.
  Location of the script codes or reference
Javascript codes are usually placed in the head tag (usually when the page would require some of the codes) or in the body tag very close to the close tag -``` </body> ``` (usually when the codes would have to access the HTML elements). Placing codes close to the ending body tag ensures that all HTML elements are loaded before the scripts are used.
 
 
 
## Syntax and Basic Constructs

### 1. Every statement should end with a semi-colon( ; )
This helps the interpreter to understand that you are done with that statement. If this symbol is omitted on that statement, you may begin to experience unexpected results. The interpreter may concatenate the next statement with the previous statement. This could result in syntax error or logical error where the result would be different than expected
 
### 2. Comments
Comments, as you have seen in other programming languages or in the previous section of this series, helps users to properly document their codes. The interpreter does not interpret comments so there could be as many comments as possible in a file. They help users to remember the purpose of certain sections of their code as well as understanding them.
 
 ```javascript
// This is a single-line comment, but guess what,
/*
  I am a comment that can span
  over
  multiple
  lines
  The interesting part is the interpreter does not try to execute me
*/
```





### 3. Statements
Javascript statements are instructions which would be executed by the browser, e.g
 ```javascript
//statements
var x = 3;
var y = 7;
var z = x + y;
alert('Wow, this is an alert!!');
```

Every line in the program above is a statement and as stated earlier, should be ended with a semi-colon.
 
A group of statements is usually a file is called a PROGRAM.
 
### 4. Whitespaces
Javascript ignores whitespaces, hence our code above could be like this
 ```javascript
//statements
var x = 3; var y = 7; var z = x + y; alert('Wow, this is an alert!!');

```
And it would still work fine. This is the more reason why every statement should end with a semi-colon. Breaking to the next line is just for readability purposes, the interpreter doesn't consider that.
 
 
 
 
 
 
### 5. Variables
Variables are like containers used for saving values. Instead of repeating a value for different uses, you could just assign it to a variable. The var keyword is used. E.g
 ```javascript

var number = 7;
console.log(number + 15);
alert(number + 15);
```

Now, if we wanted to change the number to a different value, instead of going through all areas where the number was used, I would simply change the value of the number variable.
There are other keywords for assigning variables which are let and const. These keywords came up in updated javascript.

### 6. Operators
There are so many operators in javascript of which we would cover only a few here.

#### a. Arithmetic Operators
These operators are used to perform arithmetics on numbers or variables.
The operators include Addition +, Subtraction -, Multiplication *, Division /, Modulus %, Increment ++ and Decrement --. E.g
 ```javascript

var num1 = 5;
var num2 = 6;

num1 + num2;
//returns 11

num2 % num1;
//returns 1
``` 

#### b. Assignment Operators
These operators are used to assign values to variables. They include =, /=, *=, %=, -=, +=. E.g
 ```javascript 

var num1 = 7;
// num1 would return 7

num1 += 9;
// num1 would would return 7 + 9 = 16 

```

### Resources
>[w3schools](https://www.w3schools.com/js/default.asp)

>[geeksforgeeks](https://www.geeksforgeeks.org/javascript-basic-syntax/)

>[javascripttuotorial](https://www.javascripttutorial.net/what-is-javascript/)

>[learn-js](https://www.learn-js.org/)


