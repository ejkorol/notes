# Closures

Because local bindings are re-created everytime a function is called; if that function is no longer available then we do lose that data binding unless we return it.

It is natural that local bindings are created a new every call - and different calls can't trample on one another's local binding.

You can treat functions as values.

```
function wrapValue(n) {
    let local = n
    return () => local
}
```

```
let wrap1 = wrapValue(1)
console.log(wrap1())
// -> 1
```

> The ability to be able to reference a specific instance of a local binding in an enclosing scope is called *closure*.

In other words, a function that references bindings from local scopes aronund it is called a *closure*

Closures are important, because it allows functions to retain access to variables from their parent scope, even after the parent function has finished executing.

## Use Cases

1. Data Encapsulation and Information Hiding
Create private variables and functions within a function scope and returning inner functions that have access to these variables.
2. Callback Functions
Retain access to variables from its parent scope even after the parent function has finished executing.
3. Iterating with Loops
Variable capturing with loops.
4. Memoization
Caching the results of *expensive* function calls and return the cached result when the same input occurs again to improve performance.
