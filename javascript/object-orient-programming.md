# Object Oriented Programming in Javascript

Object Oriented Programming a paradigm, or style of programming, that follows 4 key rules or concepts.
Those are largely known as the "4 Pillars of OOP":

## The Pillars of OOP:

The 4 Pillars of OOP:
1. Abstraction
2. Encapsulation
3. Inheritance
4. Polymorphism

### Abstraction

Hiding of information.

### Encapsulation

Grouping of information.

### Inheritance

The sharing of information.

### Polymorphism

Redefining of information.

## Class

```
class Person {
    constructor(name, age, height) {
        this.name = name;
        this.age = age;
        this.height = height;
    }

    sayHello() {
        return: `my name is ${this.name}`;
    }
}

let John = new Person("John", 110, 168);
```
> In this example, we are creating a class of `Person`. It is important to denote the capital syntax of the class, this stems from older object-oriented programming languages.

## Terminology

### Instance

The `instance` is created by creating a `new Class`.

### Methods

Methods are `functions` that are described within a class, and those methods then act on properties within the class.

### Constructor

A `constructor` described the properties that exist with the object *(class)* and we refer to those properties of that specific instance of the class using the `this` keyword.

The constructor is a *reserved keyword* that is invoked when a class is created.

Within the contructor we typically assign the parameters defined in the class to properties of that object.

### Inheritance

Using the `extend` keyword when initializing new classes, classes can share properties from other classes.

```
class Child extends ParentClass { /* initializing another constructor for Child */ }
```
> Here we indicate that `Child` inherits properties from `ParentClass`. In this example, `ParentClass` is a superclass or the base class and `Child` is the subclass.
