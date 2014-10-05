Web Lession 4 - More JavaScript
=========

We've covered about half of the JavaScript basics, here's the rest.

**Estimated Time** - 45 min

[TOC]

## Prereqs

- Web Lesson 3

## If Statements, For Loops, and While Loops

Last lesson you had to look up if statements and for loops for the questions, so we'll only touch on them here. While loops are new, but are pretty simple.

### If Statements

If statements are just forks in the road. If something, do this, else do this other thing.

```
function isTrue(value) {
    if (value == true) {
	    console.log('Yes');
	} else {
	    console.log('No');
	}
}
isTrue(true);
isTrue(false);
```

#### Else If

If there's not just two forks in the road you can have multiple paths.

```
function numberTest(num) {
    if (num == 1) {
	    console.log('Number is 1');
	} else if (num == 2) {
	    console.log('Number is 2');
	} else if (num == 10) {
	    console.log('Number is 10');
	} else {
	    console.log('Other number');
	}
}
numberTest(1);
numberTest(2);
numberTest(3);
numberTest(10);
```

#### Logical Operators

Something that was glazed over above was how `num == 1` is evaluated. `==` is a logical operator which will return a **boolean** value: true if the values are equal, false otherwise. Take a look at this [W3 Schools article](http://www.w3schools.com/js/js_comparisons.asp) (**NOTE:** W3 Schools is good for basic stuff, but not the best for advanced things, so don't get attached to it) about logical operators and how they can be combined.

Some of the fun of JavaScript is that logical operators try to get tricky sometimes. Things can happen which you wouldn't expect. Some of the questions below cover some of this.

### For Loops

For loops are already covered on the web, so take a look at [W3 Schools](http://www.w3schools.com/js/js_loop_for.asp) again.

### While Loops

Same for [while loops](http://www.w3schools.com/js/js_loop_while.asp).

## Arrays and Objects

Numbers, strings, and booleans are pretty simple, but arrays and objects can get a little more difficult.

### Arrays

Arrays are just a collection of items. The items can be of any type and are accessed by referencing which place in the array the item is in. For example:

```
var array = [1, true, 'seven'];
console.log(array[1]);
```

The console should show true because array indicies start at 0. Arrays have a few special properties such as **length** which you can access (e.g. `array.length`).

#### Functions

Arrays have a lot of useful function attached to them by default. The way these are attached is a bit complicated (look up "javascript prototype" if you're interested), but we don't normally have to worry about that. Look up the following functions and try them out:

- slice
- splice
- push
- pop
- sort
- join
- indexOf

There are a few others, but these are the most useful in my opinion.

### Objects

Objects are the most generic data type. They are essentially the "everything else" bucket and are very flexible. Normally, objects we create are simple key-value pairs. For example:

```
var obj = {'myKey': 'myValue'};
```

In the simple example above the key is 'myKey' and the value is 'myValue'. This in particular isn't terribly profound, but the fun part is that values can be anything: numbers, strings, arrays, other objects, and even functions. This means you can have highly nested objects which contain a whole bunch of stuff.

The way you access the values of an object is by referencing the key:

```
var obj = {'myKey': [1, 2, true]};
console.log(obj.myKey);
console.log(obj['myKey']);
```

You'll notice both ways of accessing a key work. Each way is convinient in it's own circumstances and should be used appropriately.

## Assignment

### Questions

Answer the following questions:

- What does `1 == '1'` result in? (e.g. `console.log(1 == '1')`)
- What does `!0` result in?
- What does `1 === '1'` result in?
- What happens if you try to access the 5th element of an array which only has 3 elements?
- What happens if you try to access the value of an object with a key that it doesn't have?

If some of the answers above suprise you, look up why they do what they do. A good place to start is looking up "JavaScript falsy values".

### Code

Write a function for each of the following:

- A function which takes two inputs and returns an array of those two inputs (e.g. 5, 2 -> [5, 2])
- A function which takes in an array and returns the first element
- A function which takes in an array and returns the first element, but returns `undefined` if the input is not an array or the array has no elements
- A function which takes in an array and returns the length of the array
- A function that takes in an array and returns a string of all the elements joined by a comma (e.g. [1, 2, 3] -> '1,2,3')
- A function which takes in an object and returns the keys of the object

## End

Now you've got a little experience with the JavaScript basics. If you are a little fuzzy on any of the parts above take the time to look them up, there's plenty of documentation out there. From now on we'll be building on everything in this lesson and the last.