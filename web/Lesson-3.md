Web Lession 3 - Some JavaScript
=========

Static web pages are good, but web pages which do things are cooler.

**Estimated Time** - 30 min

[TOC]

## Prereqs

- Web Lesson 2

## Script Tags

The easiest way to insert JavaScript into a page is to throw a `<script></script>` block in and put some JavaScript inside of it. For instance, make a new web page with the following code in it and open it in a browser.

```
<html>
	<body>
		<script>
			alert('Wat');
		</script>
	</body>
</html>
```

Pretty fancy. You can throw anything inside a script tag and the browser will run the code as soon as it reaches that block. In this case the browser threw an alert with the string 'Wat'.

## JavaScript Basics

The easiest way to test JavaScript is to put it in a block like the one above. For now it will be assumed that the code examples will be placed inside `<script>` tags.

### Console.log

`console.log()` is a great way to see what's happening while your code is running. For example, test out the following code.

```
console.log('Hello');
```

Nothing happened, right? That's because we need to open up the console to see what is getting logged. In Chrome or Firefox right click on your page and click **Inspect Element**. A window will pop up and one of the tabs is **Console**. Now you should see 'Hello' in the console. Logging variables and strings is a good, basic way to debug.

### Comments

Comments in code don't get executed. You can use comments to add explanations of your code for other humans to read, or to hide code you don't want to execute. I use them a little below, so I figured I should mention them. Inline comments use `//` and block comments use `/* */`. For example:

```
console.log('Hello'); // I won't get executed
/*
Neither will I
*/
// Or this console.log('Goodbye');

```

### Variables

If you've coded in any language before you're probably familiar with variables. They just store values. A simple example of using a variable is shown below.

```
var myVariable = 'Hello';
console.log(myVariable);
```

As you might guess, you should see 'Hello' in the console because we logged our variable which has been set to the string 'Hello'.

#### Data Types

In JavaScript you don't have to define what data type a variable is. This is a double edged sword. For those of you not familiar with data types I recommend looking up the following JavaScript data types:

- string
- number
- boolean
- array
- object

The first three are pretty self explanatory, but **objects** can get a little abstract at times.

Not defining data types is cool because everything is a `var`. You don't have to worry about fixing what type a variable will be up front which means we can be lazy.

The other side of this is that errors don't get caught when they should. Imagine the following scenario:

```
var num = 5;
// Some stuff happens
num = 'Whoops';
// Some other stuff
console.log(num / 5);
```

Hmm. An error is probably going to get thrown during that `console.log()` because you can't divide a string by 5, but that's not really where the problem was. Have fun figuring out that you accidentally reassigned `num` to a string in the middle of your code. If JavaScript was a [strongly typed language](http://en.wikipedia.org/wiki/Strong_and_weak_typing) you wouldn't have been able to reassign `num` in the first place, but I digress...

### Functions

Functions make the world go round. You could type out JavaScript in one huge block, but what if you want to reuse code or test it? Functions make it a lot easier to compartmentalize your code, so let's make some.

```
function hello() {
    console.log('Hello');
}
hello();
```

Pretty simple. First we defined a function named **hello** which took no arguments (we'll cover those in a second) and simply logged 'Hello' to the console. We then executed our function by calling `hello()`.

#### Arguments

Sometimes functions need inputs. We'll define these inputs as variable names which we can use within the function. For example:

```
function helloAgain(name) {
    console.log('Hello ' + name);
}
helloAgain('Brian');
```

Our **helloAgain** function now takes an argument which we can refer to as **name** within the function. When we call our function we can now pass an argument to it which gets used within the function. The **+** operator on strings concatonates them, so we should see 'Hello Brian' in the console.

##### Aside

Astute readers will notice the arguments are not typed (e.g. `function hello(String name) { ... }`). Weak typing FTW.

#### Return

Each function can return an output after it is finished. For example:

```
function multiply(a, b) {
    return a * b;
}
console.log(multiply(5, 2));
```

You should see in the console 10. The **multiply** function takes in both inputs, returns their product, and then `console.log()` logs that result.

## Assignment

### Questions

Answer the following questions:

- What happens if you call a function which requires an input without an input (e.g. call **helloAgain** with no input)?
- What happens if you pass more inputs into a function than it is expecting?
- What happens if you pass an input of a different datatype into a function than it is expecting? (e.g. `helloAgain(true)`)

You will probably find that some of the answers make sense and some of them don't. JavaScript takes care of a lot of things for you, but these can get you in trouble sometimes. Like the variable example shown above some errors don't get thrown when they should and bubble up later, making debugging a nightmare. Just keep this in mind as you write JavaScript.

### Code

Write a function for each of the following:

- A function which logs 'Even' if the input is even and 'Odd' if the input is odd
  - **Hint:** Look up **if** statements
- A function which does the same as the previous function but logs 'Neither' if the input is not a number
  - **Hint:** Look up **typeof**
- Create a function which takes in a number and logs each number between 0 and the input
  - **Hint:** Look up **for** loops

## End

You should now know the basics of JavaScript and have an understanding of functions, variables, and how to use them. You should also know a little about **if** statements and **for** loops. We'll touch on these a little in the next lesson.