# Promises

Promises are an abstract concept. Instead of arranging a function to be called sometime in the future, you return a `promise` object that represents an object in a *future event*.

A `Promise` is an asynchronus action that may complete as some point and produce a value, it is then able to notify anyone who is interested when it's value is available.

## Synchronus Functions

Refers to code that executes one a time, from the first line to the last line.

The program will wait for the current line to execture before moving onto the next.

However, what if one line takes a really long time to execute?

*Synchronus code*

```
console.log("I am first");
console.log("I am second");
console.log("I am surgeon");
```

```
[Task 1] -> [Task 2] -> [Task 3]
```

## Asynchronus Execution

Allows you to run a task in the 'background'.

Programs will be responsive to other events while the task runs,

Lastly, asynchronus code may execute in any order.

## The Promise Object

### Axios

Calling an `axios` method without the `await` keyword return a `Promise` object.

The data is not available right away, however will be made available in the future.
