# Parameters

To make a function more reusable you'll often want to pass information into it. These inputs are called **parameters**.

Let's say we wanted to change our *displayGreeting* function from the last example to be able to greet a specific person, instead of printing "Hello, world!" each time we call the function. We can use a parameter to specify the name. A parameter (also sometimes called an argument), is additional information sent to a function.

Parameters are listed in the definition of the function within parenthesis. There can be multiple parameters, comma separated like so:

```javascript
function name(param, param2, param3) {

}
```

We can update our displayGreeting function to take a name as input, and have a customized message print to the console.

```javascript
// function with a parameter called name
function displayGreeting(name) { 
    // creating a new local variable that inserts the name into a string   
    const message = `Hello, ${name}!`; 
    // printing the variable to the console
    console.log(message);
}
```

When we want to call our function and pass in the parameter, we specify it in the parenthesis.

```javascript
displayGreeting('Christopher');
// displays "Hello, Christopher!" when run
```

## Default values

We can make our function even more flexible by adding more parameters. But what if we don't want to require every value be specified? Keeping with our greeting example, we could leave name as required (we need to know who we're greeting), but we want to allow the greeting itself to be customized as desired. If someone doesn't want to customize it, we provide a default value instead. To provide a default value to a parameter, we set it much in the same way we set a value for a variable - `parameterName = 'defaultValue'`. To see a full example:

```javascript
function displayGreeting(name, salutation='Hello') {
  console.log(`${salutation}, ${name}`);
}
```

When we call the function, we can then decide if we want to set a value for salutation.

```javascript
displayGreeting('Christopher');
// displays "Hello, Christopher"

displayGreeting('Christopher', 'Hi');
// displays "Hi, Christopher"
```

## Return values

Up until now the function we built will always output to the [console](https://developer.mozilla.org/en-US/docs/Web/API/console). Sometimes this can be exactly what we're looking for, especially when we create functions which will be calling other services. But what if I want to create a helper function to perform a calculation and provide the value back so I can use it elsewhere?

We can do this by using a return value. A return value is returned by the function, and can be stored in a variable just the same as we could store a literal value such as a string or number.

If a function does return something then the keyword `return` is used. The `return` keyword expects a value or reference of what's being returned like so:

```javascript
return myVariable;
```

We could create a function to create a greeting message and return the value back to the caller

```javascript
function createGreetingMessage(name) {
  const message = `Hello, ${name}`;
  return message;
}
```

When calling this function we'll store the value in a variable. This is much the same way we'd set a variable to a static value (like `const name = 'Christopher'`).

```javascript
const greetingMessage = createGreetingMessage('Christopher');
```
