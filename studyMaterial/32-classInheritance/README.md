# 32. Class, Inheritance
## Classes and Objects:
A class is a blueprint with which objects/variables are created. It is a custom data type containing properties and methods. An object is an instance of a class that uses the class’s methods and properties. Let’s understand and implement this via javascript:
```javascript
class Animal{
    constructor(name){
        this.name = name;
    }
}
// Let's create Object from the class Animal
var animal = new Animal("Dog");
```
A constructor is a special keyword reserved to create a constructor function. A constructor function is always called automatically upon the creation of an object/instance of a class. It implicitly returns an instance of the newly created object. A default constructor is built-in to the class and we override it by implementing our own. The new keyword is necessary to use with object creation as it will tell the compiler to invoke the constructor function.

In Javascript, we can create Objects using functions without the use of the class keyword.
```javascript
function Animal(name){
    this.name = name;
}
var animal = new Animal("Dog");
```
This is how we create Objects from functions and classes in javascript.

## Inheritance:

Inheritance is an important concept in Object Oriented Programming paradigm. It’s a process by which child objects inherit the properties of the parent object. In javascript, inheritance is built into objects and every object has a property called prototype which refers to the parent of that object and this chain goes up until the prototype points to null.

![](/studyMaterial/32-classInheritance/protot.webp)

As you can see above, the Obj has a default prototype property referring to Object which is a built-in data type.

Now let’s implement inheritance via classes and objects:
```javascript
class Person{
    constructor(name){
        this.name = name;
    }
    sayName(){
        console.log(this.name);
    }
}
class Student extends Person{
    constructor(name, rollNumber){
        super(name);
        this.rollNumber = rollNumber;
    }
    logDetails(){
        console.log(`Name: ${this.name}, Roll number: ${this.rollNumber}`)
    }
}
var student = new Student("Heisenberg", 1);
student.logDetails();    // Name: Heisenberg, Roll number:1
student.sayName();       // Heisenberg
```

Student class has access to all properties of the person class.

## Resources

https://medium.com/codex/oop-in-javascript-encapsulation-inheritance-polymorphism-abstraction-and-association-2cbcd93bbb4f
https://www.simplilearn.com/tutorials/javascript-tutorial/oop-in-javascript
https://www.indeed.com/career-advice/career-development/what-is-object-oriented-programming
https://www.tektutorialshub.com/javascript/prototype-in-javascript/

