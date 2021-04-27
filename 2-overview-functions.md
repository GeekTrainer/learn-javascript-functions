# Functions

At its core, a function is a block of code we can execute on demand. This block of code might perform a task, such as navigate to a different part of a website, or calculate a value, like the sum of two numbers. Functions are also perfect for scenarios where we need to perform the same task multiple times; rather than duplicating the logic in multiple locations (which would make it hard to update when the time comes), we can centralize it in one location, and call it whenever we need the operation performed - you can even call functions from other functions!

Just as important is the ability to name a function. While this might seem trivial, the name provides a quick way of documenting a section of code. You could think of this as a label on a button. If I click on a button which reads "Cancel timer", I know it's going to stop running the clock.

## Creating and calling a function

A function takes some input, an and returns an output that somehow transforms the input. For example, an addition function could take in two integers, and return the sum of their values.

There are a couple of different components that make up a function:

* The **function body** is the block of code that will begin executing when the function is called.
* A **parameter** is another name for the input that's passed to a function.
* Finally, there is some **return** value, or the output of the function.

The syntax for a function looks like the following:

 ```javascript
 function nameOfFunction(parameter) { // function definition with some input
 // function body
}
 ```

To start, let's check out some basic functions that don't take any inputs or return any values. If I wanted to create a function to display a greeting in the debugging [console](https://developer.mozilla.org/en-US/docs/Web/API/console) of your code editor, it might look like this:

```javascript
function displayGreeting() {
  console.log('Hello, world!');
}
```

The function above is called *displayGreeting*, and when we run the function, the text "Hello, world!" will be printed to the console.

Whenever we want to call (or invoke) our function, we use the name of the function followed by (). It's worth noting the fact our function can be defined before or after we decide to call it; the JavaScript compiler will find it for you.

```javascript
// calling our function
displayGreeting();
```

> [!NOTE] There is a special type of function known as a method, which you've already been using! In fact, we saw this in our demo above when we used console.log. What makes a method different from a function is a method is attached to an object (console in our example), while a function is free floating. You will hear many developers use these terms interchangeably.

## Best practices

There are a handful of best practices to keep in mind when creating functions:

* As always, use descriptive names so you know what the function will do
* Use camelCasing to combine words
* Keep your functions focused on a specific task