# Lesson #3: JavaScript Overview

JavaScript is a programming language created in 1995 by Brendan Eich, working for Netscape, with the goal of making websites more dynamic. Today, it is used across millions of websites and devices worldwide, for a wide range of use cases, including web servers, offline apps, IoT devices, command line tools, and other non-web projects.

As a general purpose language, JavaScript is capable of accomplishing nearly any computing task you wish to program. Although it started off in web browsers, and that remains a common use for it, JavaScript is a good choice for many types of automation and scripting projects, especially when you want to build a prototype and get something working quickly. It can be used to build simple tools and widgets or complex apps like games and music software.

## Contents

 - Hello World
 - Basic math
 - Mutiple statements
 - Variable assignment

## Hello World

A [Hello World](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program#Time_to_Hello_World) program is the simplest code that can be written in a given programming language. It is named such because the goal is to write a program that, when executed, causes that message to be shown on the screen.

In JavaScript, Hello World looks like this:

```js
console.log('Hello, World!');
```

Save the code above to a file named `hello.js`. Then use Node to execute it by running the command below in your terminal.

*__Tip:__ For this to work, the current working directory in your terminal must be the directory where you saved the hello.js file. Refer to Lesson 1 for how to change your working directory.*

```console
$ node hello.js
```

If it worked, you should see "Hello, World!" in your terminal (without the quotes). Congrats, you wrote your first JavaScript program!

Showing this message in the terminal is not only an important first step to achieve, it's also a powerful one. Many of the world's most useful programs involve little more than simple text-based I/O (input and output) on the screen. For example, a database that stores data about your friends (i.e. an address book) just needs to show some text formatted as a table with rows and columns. You are on your way to being able to write a program like that!

Here is how the Hello World example above works:
 - `console.log()` is a _function call_. Doing this causes the built-in log function to execute. The log function is a feature provided by Node.js that allows us to show a message on the screen. All we have to do is give it the message that we want to show.
 - Between the parentheses, we passed an _argument_ to the log function in the form of a _string_, whose value is "Hello, World!". This is how we tell the log function what to show. An argument is any piece of data that you provide to a function. A string is simply a list of characters. We could have instead logged other types of data, such as a number, a boolean like `true` or `false`, etc.

## Basic math

Let's make the computer do some proper computation.

```js
console.log(1 + 2);
```

Save the code above to a file named `sum.js`. Then use Node to execute it by running the command below in your terminal.

```console
$ node sum.js
```

If it worked, you should see `3` in your terminal. Yay, three cheers for math!

## Multiple statements

Up until this point, the programs you have written contained only a single instruction, otherwise known as a statement. As you can imagine, most programs need to be longer than one statement to do something useful. Going forward, we will start writing programs with multiple statements.

In JavaScript, statements are separated by a `;` semicolon. Additionally, to improve readability, statements are usually separated by a new line after the semicolon.

## Variable assignment

Variables are an important part of programming, just as they are in math. They help re-use the result of previous computations, which makes it easier to write programs that are resiient and flexible to change.

```js
const answerToLife = 40 + 2;
console.log(answerToLife);
```

In the example above, we create a new variable named `answerToLife` and assign the number `42` as its value. By using `const`, we have made the variable a _constant_, which simply means that the variable cannot have a new value assigned to it after it is created.

In most cases, it is best to use a constant in order to avoid accidentally changing its value. However it is possible to create variables whose values are allowed to change within the program. These are often referred to as _mutable_ variables and they are created by using the keyword `let` instead of `const`.

```js
let answerToLife = 40 + 2;
console.log(answerToLife);
answerToLife = 3.14;
console.log(answerToLife);
```

Save the code above to a file named `life.js`. Then use Node to execute it by running the command below in your terminal.

```console
$ node life.js
```

If it worked, you should see `42` in your terminal, followed by `3.14` on a new line. As you can see, the value of the variable has clearly changed, as we logged the same variable twice and it showed a different number each time.

Now try doing the same thing, except use a constant instead of a mutable variable. You should see an error in your terminal, because you cannot assign a value to a constant after it is created, so the program fails on the third line.

You can create as many variables in your program as you want to, so it's usually better to create a new constant instead of changing the value of an existing variable. That also forces you to think carefully about the names of your variables, what they represent, and how they are different from one another.

## Next up

When you are done with this lesson, proceed to [Lesson #4: JavaScript Types](../04-types/README.md).
