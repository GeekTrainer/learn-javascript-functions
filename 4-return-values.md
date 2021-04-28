Up to this point, the functions we've built have always output to the [console](https://developer.mozilla.org/en-US/docs/Web/API/console). Sometimes this can be exactly what we're looking for, especially when we create functions which will be calling other services. But what if I want to create a helper function to perform a calculation and provide the value back so I can use it elsewhere?

We can do this by using a return value. A return value is returned by the function, and can be stored in a variable just the same as we could store a literal value such as a string or number.

If a function does return something, the keyword `return` is used. The `return` keyword expects a value or reference of what's being returned. Here's an example:

```javascript
return myVariable;
```

We could create a function to create a greeting message and return the value back to the caller. Note that the `return` keyword stops the execution of a function and returns the specified value, so you usually want to use it at the end of your function, like so:

```javascript
function createGreetingMessage(name) {
  const message = `Hello, ${name}`;
  return message;
}
```

> [!NOTE] Variables defined inside a function can't be accessed from anywhere outside of the function. These variables are called **local variables**, and outside of the function, they are considered **out of scope**.

When calling this function we'll store the value in a variable. This is much the same way we'd set a variable to a static value (like `let name = 'Christopher'`).

```javascript
let greetingMessage = createGreetingMessage('Christopher');
```

Return values help demonstrate another reason why functions are such an important part of JavaScript - you can reuse the same function with different arguments to produce multiple return values.
