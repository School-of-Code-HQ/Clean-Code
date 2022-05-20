# Styling and Formatting Guide

<img src="images/soclogo.png"  width="150" height="150">

## Table of Contents

1. [Introduction](#Introduction)
2. [Naming Conventions](#Naming-Conventions)
3. [Indentation & Spacing](#Indentation-And-Spacing)
4. [Brackets & Colons](#Brackets)
5. [Comments](#Comments)
6. [Code Formatter](#Code-Formatters)

## Introduction

In this introductory guide, we will look at why coding practices are important, why formatting your code is important, and how you can achieve well formatted, easy to understand code.

Code doesn't need to look good or read well to work. So why bother? Let's take a look at the following code.

```js
function a(b,c){return(b/c*100)}const x=1;const y=2;const b = a(x,y);
```

🤮 - this works. But the code is not easy to work with as a programmer. Formatting and code style practices are almost always solely to make it easier for code to be quickly read and understood. Here's the same code as above but with a few minor tweaks in style (the functionality is exactly the same);

```js
function calculatePercentage(amount, total) {
  return (amount / total) * 100;
}

const numMentors = 1;
const numPeople = 2;

const percentageOfPeopleWhoAreMentors = calculatePercentage(numMentors, numPeople);
```

Easy to read code is good news not just for you, but any other developers who will look at the code in the future. Well structured, well formatted, and well written code can also help make errors in your code more obvious.

Let's look at some of the techniques and ideas of how we can achieve code that doesn't make us cry when we look at it 😢

## Naming Conventions

Using good, descriptive names for your functions and variables can reveal the intention of the code at a glance. This means it reduces the effort and time needed to read that code and understand what it is doing. This means that you are likely to understand the code better, quicker, which means less mistakes and more holidays 🏖

Remember to always use meaningful names so your code speaks for itself.

### Function Names

**Bad:**

```js
function find(name) {}
```

**Good:**

```js
function findBooksByAuthor(author) {}
```

### Variable Names

**Bad:**

```js
let someStuff = ["Bananas", "Bread", "Cheese", "Crisps", "Milk"];
```

**Good:**

```js
let shoppingList = ["Bananas", "Bread", "Cheese", "Crisps", "Milk"];
```

**[⬆ back to top](#table-of-contents)**

## Indentation And Spacing

### Indentation

You can think of indentation as the distance from the page edge. Indentation is the leading whitespace before the code. Indentation has no meaning in JavaScript - the computer will ignore it completely. However, although your code will run without it, good indentation helps improve code readability.

Statement with the same indentation level(whitespace) should be treated as a single code block.

#### Examples

Indentation can help us see the relationships in code.

```html
<body>
  <h1>Hello</h1>
  <h2>There</h2>
</body>
```

In the HTML code above, we can see from the indentation that `body` has some children, and the `h1` and `h2` "belong" to the body and are at the same level.

The same approach can be useful in JavaScript.

```js
let myName = "Kazeem";
if (myName === "Kazeem") {
  console.log(myName); //this is indented because it's treated as a separate code block.
}
myName = "Ade";
```

Above, we can see that the indented code belongs to the if statement. This tells us at a glance that the code will only run if the condition evaluates to `true`.

```js
const names = ["kazeem", "chris", "Liz"];
for (let i = 0; i < names.length; i++) {
  console.log(names[i]); //this is indented because it's treated as separate code block.
}
```

In the for loop example, we can quickly see that the indented code is what will be repeated by the loop. Although brackets are important, it can be fiddly to see which brackets line up with which. The indentation here makes is speedy and easy to see what code belongs where, and when it will run. That's amazing 🤯

### White Space

White space is mostly irrelevant to JavaScript (unless it separates key words, or is in a string). This means that most white space gives us the opportunity to make our code more readable.

Bad:

```js
const names=["kazeem","chris","Liz"];
const favouriteLanguage="Python";
```

Good:

```js
const names = ["kazeem", "chris", "Liz"];
const favouriteLanguage = "Python";
```

Although some of this is opinionated, it's widely thought that space allows our eyes to scan and identify items of interest more easily that clutter. Hopefully you'll agree, and space things out where possible.

### Line Space

If white space is the space between things on the same line, line space is the space between those lines. As always, it's important to be consistent when spacing so that you can get used to understanding your code at a glance.

Bad:

```js
function(num1,num2){
console.log(num1*num2)
}
function(firstName){
console.log(firstName)
}
function(food){
console.log(food)
}
```

Good:

```js
function(num1,num2){
  console.log(num1*num2)
}

function(firstName){
  console.log(firstName)
}

function(food){
  console.log(food)
}
```

## Brackets

There are three main types of brackets in JavaScript. They are parenthesis `()` (or smoothies as we say at School of Code 🥤), square brackets `[]` (squaries? 🧐), and curly brackets `{}` (or as we call them, *squiggs* 🥴). This section shows what they do and how you can use them.

#### Parenthesis ()

You can think of smoothies as the collectors. They can show things being collected together for evaluation.

```js
const answer = 4 * (2 + 3);
```

They can collect together the parameters of a function as they are defined.

```js
function yourFavoriteStuffOnScreen(movie, tv) {}
```

In the same way, they can be used to collect the condition of an `if`, `else`, `for` loop, `while` loop, etc.

```js
for (let i = 0; i < array.length; i++) {
  console.log(i);
}
```

They can be used to call a function and collect the arguments to pass through to it.

```js
yourFavoriteStuffOnScreen("The Avengers", "The Simpsons");
```

#### Square Brackets []

Square brackets are mainly used for either:

1. Defining an array
2. Accessing items in an array
3. Accessing properties in an object

##### Defining an array

```js
const positiveNumbers = [1, 2, 3, 45, 6, 77];
```

##### Accessing items in an array

```js
const positiveNumbers = [1, 2, 3, 45, 6, 77];
positiveNumbers[0]; // gets 1 from the array
positiveNumbers[2]; // gets 3 from the array
```

##### Accessing items in an object

Square brackets can be used to get the value of a key in an object. This does the same thing as using dot(.) notation to get the values.

```js
const coachesRunningSpeed = {
  kazeem: 15,
  jordan: 18,
  arshi: 17
};

coachesAge["kazeem"]; // gets the value of kazeem from the object (15)
coachesAge.kazeem; // gets the value of kazeem from the object (15)
```

#### Curly Brackets {}

Curly brackets are used to open and close code blocks. Code blocks are present in things like loops, if/else statements, and functions. They define statements to be executed together.

Curly brackets also relate to objects. They allow us to define an object, or to destructure properties from an object.

Below, the code in the curly bracket runs if the condition in the parenthesis is met.

```js
const yourName = "Kazeem";
if (yourName === "Kazeem") {
  console.log(yourName);
}
```

```js
const scores = { 
  kazeem: 12,
  jordan: 15
};

const { kazeem } = scores; // makes a new variable called kazeem, with a value of 12 because the object has a property of kazeem with that value
```

**[⬆ back to top](#table-of-contents)**

## **Comments**

### How to leave comments like a pro!

Comments save time, help other developers navigate through your code, and help your future self understand what you had written.

This is especially true when you are learning. When you hit real-world projects, often the preference is to have code that explains itself. If your code needs comments to explain it, it might be too complicated.

In JavaScript you create a single-line comment with `//` and multi-line comments using `/*` and `*/`.

#### As you can see from the examples below, comment overkill can be overwhelming and take to long to read through and understand.

**Bad:**

```js
function printMessage() {
  //calls a function
  const comment = document.getElementbyID("comments").value; // declares a variable
  if (comment != null && comment != "") {
    //starts an if statement if there's a comment
    return console.log("What a meaningful comment"); //prints a string to the console
  }
}
```

**Good:**

```js
//checks to see if there's a comment. If so, returns a message.
function printMessage() {
  const comment = document.getElementbyID("comments").value;
  if (comment != null && comment != "") {
    return console.log("What a meaningful comment");
  }
}
```

**[⬆ back to top](#table-of-contents)**

## Code Formatters

### WHY WE USE FORMATTERS:

Remembering all the rules about code formatting can be taxing so thats where code formatters can help!

Code formatters automatically format code for you depending on the preferences you set. Automatic formatting enables higher code quality, especially when you are working in teams and other people are reading the code you’ve written. Many developers maintain standards of code formatting like 2-space or 4-space indentation or using single or double quotes. This helps with both readbility and finding errors. 

Two examples of code formatters are Prettier, which is used to keep your coding style consistent and ESLint, which helps detect formatting issues and find inconsistencies in your code.


Installation ans setup guides for Prettier and ESLint:

Prettier Configuration:<br>
https://www.digitalocean.com/community/tutorials/code-formatting-with-prettier-in-visual-studio-code

ESLint Configuration:<br>
https://eslint.org/docs/user-guide/getting-started

Using both of these tools together can be a very effective way to maintain high quality code but may cause conflict. The following guide will help you successfully intergrate both tools succesfully.
https://prettier.io/docs/en/integrating-with-linters.html


**[⬆ back to top](#table-of-contents)**
