# Lesson #4: JavaScript Types

In the context of programming, there are various data "types", or categories of data that we want to manipulate: text, numbers, true/false values, etc. Each of these have different characteristics in terms of what we can do with them and how they are useful.

In JavaScript, there are seven basic types, which are often referred to as the "primitive" types:

 - Boolean
 - Number
 - String
 - Undefined
 - Null
 - BigInt
 - Symbol

Note that `BigInt` and `Symbol` are rarely used, so we will only cover them briefly. The others are important to understand in detail.

## Boolean

A boolean is a value that represents logical `true` or `false`. These are useful for yes/no answers, on/off states, and other situations where your program has some data that can only be in one of two states.

Booleans can be created directly, by using literal `true` or `false` as a value, or they can be created as the result of a comparison operation, such as `1 === 2` or `1 > 2`, which both evaluate to `false`.

```js
const isProgrammingAwesome = true;
console.log(isProgrammingAwesome);
const isThreeLessThanTwo = 3 < 2;
console.log(isThreeLessThanTwo);
```

## Number

A number is a numeric value, such as `1`, `2`, or `3`. However, numbers can be quite tricky for computers to deal with. That is because, while us humans can understand the concept of very large numbers and [irrational numbers](https://en.m.wikipedia.org/wiki/Irrational_number), we don't actually have infinite computer memory, computing time, or other computing resources. Many optimizations and compromises are made to do math efficiently on a computer and this has lead to many different ways of representing numbers within programming languages. In JavaScript, all numbers are in a [64-bit floating-point](https://en.wikipedia.org/wiki/Double-precision_floating-point_format) format, as specified by the [IEEE 754](https://en.wikipedia.org/wiki/IEEE_754) standard, which determines how precise numbers are able to be as well as how arithmetic is performed.

IEEE 754 has the advantage of being very effecient, however it is notoriously bad at being precise in certain situations involving decimals. A commonly cited example of this is the result of `0.1` + `0.2`, which evaluates to `0.30000000000000004`, effectively a rounding error. That can lead to strange results, as seen below, if you are checking for the result of an equation to be a specific decimal value.

```js
console.log(0.1 + 0.2 === 0.3);
```

In everday use, this is not a significant problem, because most programs will simply round the result or discard such tiny fractions. You can also work around the problem by always doing math with whole integers instead of fractions. However, it is important to be aware of this before writing a program where precision is important, such as financial software.

## String

A string is a list of characters. In JavaScript, strings are created by surrounding the text with quotes.

```js
const myName = 'Seth';
```

You can access individual characters within the string by referencing the index of the character. The first character is at index zero.

```js
const myName = 'Seth';
const firstLetter = myName[0];
console.log(firstLetter);
```

## Next up

When you are done with this lesson, proceed to [Lesson #5: JavaScript Loops](../05-loops/README.md).
