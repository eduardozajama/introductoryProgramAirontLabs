# 33. Encapsulation & Polymorphism

## Encapsulation
Encapsulation means hiding information or data. It refers to the ability of the object to execute its functionality without revealing any execution details to the caller. In other words, the private variable is only visible to the current function and is not accessible to the global scope or other functions.
```javascript
const Book = function(t, a) {
   let title = t; 
   let author = a; 
   
   return {
      summary : function() { 
        console.log(`${title} written by ${author}.`);
      } 
   }
}
const book1 = new Book('Hippie', 'Paulo Coelho');
book1.summary();
```
```
> Hippie written by Paulo Coelho.
```
In the above code the title and the author are only visible inside the scope of the function Book and the method summary is visible to the caller of Book. So the title and the author are encapsulated inside Book.

## Polymorphism
The ability to call the same method on different objects and have each of them respond in their own way is called polymorphism.
```javascript
let book1 = function () {}
book1.prototype.summary = function() {
   return "summary of book1"
}
let book2 = function() {}
book2.prototype = Object.create(book1.prototype);
book2.prototype.summary = function() {                 
   return "summary of book2"
}
let book3 = function() {}
book3.prototype = Object.create(book1.prototype);
book3.prototype.summary = function() {
   return "summary of book3"
}
   
var books = [new book1(), new book2(), new book3()];
books.forEach(function(book){
   console.log(book.summary());
});
```
```
> summary of book1
> summary of book2
> summary of book3
```
Relationships between the objects will be defined by Association, Aggregation, and Composition.

### Association
Association is the relationship between two or more objects. Each Object is independent. In other words, association defines the multiplicity between objects: one-to-one, one-to-many, many-to-one, many-to-many.
```javascript
function Book(title, author) { 
   this.title = title; 
   this.author = author; 
}
const book1 = new Book ('Hippie', 'Paulo Coelho');
const book2 = new Book ('The Alchemist', 'Paulo Coelho');
book2.multiplicity = book1

```
book1 was assigned to the property of multiplicity to object book2. It shows the relationship between objects book1 and book2. Both can be added and removed independently.

### Aggregation
Aggregation is a special case of an association. In the relationship between two objects, one object can have a more major role than the other. In other words, when an object takes more ownership than another one, that is aggregation. The owner object is often called the aggregate and the owned object is called the component. Aggregation is also called a “Has-a” relationship.
```javascript
function Book(title, author) { 
   this.title = title; 
   this.author = author; 
}
const book1 = new Book ('Hippie', 'Paulo Coelho');
const book2 = new Book ('The Alchemist', 'Paulo Coelho');
let publication = {
   "name": "new publication Inc", 
   "books": []
}
publication.books.push(book1);
publication.books.push(book2);

```


book1 and book2 were added to books under publication object. If the publication object is deleted until book1 and book2 are available, then both Book and publication live independently.

### Composition
Composition is a special case of aggregation. Composition is when an object contains another object and the contained object can’t live without the container object.
```javascript
let Book = {
   "title": "The Alchemist", 
   "author": "Paulo Coelho",
   "publication": {
      "name": "new publication Inc",
      "address": "chennai"
   }
}

```
Here the property publication is strictly bounded with the Book object, and publication can’t live without theBook object. If the Book object id was deleted, then the publication would also be deleted.
## Resources

https://medium.com/codex/oop-in-javascript-encapsulation-inheritance-polymorphism-abstraction-and-association-2cbcd93bbb4f
https://blog.sessionstack.com/how-javascript-works-3-types-of-polymorphism-f10ff4992be1
https://www.javatpoint.com/javascript-oops-polymorphism

https://www.indeed.com/career-advice/career-development/what-is-object-oriented-programming
https://betterprogramming.pub/object-oriented-programming-in-javascript-b3bda28d3e81


