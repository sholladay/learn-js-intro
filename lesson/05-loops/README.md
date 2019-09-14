# Lesson #5: JavaScript Loops

When we want to run a block of code more than once, a convenient way to do it is to use a loop.

## `while` loops

The simplest type of loop is a `while` loop. It takes an expression, checks if the result is truthy, and if so, then the block of code inside of the loop is executed. This procedure is repeated continuously, checking the expression between each iteration of the loop, until the result of the expression is a falsey value.

When using a `while` loop, a common mistake is to use a condition that always returns `true`. It is important to ensure that the condition eventually becomes `false`, otherwise you will have an infinite loop on your hands! An infinite loop is a loop that runs forever, potentially freezing your computer by constantly keeping your CPU busy. If you think this may be happening, exit your program as soon as possible (in a terminal, this can be done with <kbd>Control</kbd> + <kbd>C</kbd>).

Let's count from zero to four.

```js
let i = 0;
while (i < 5) {
    console.log('I can count to ' + i);
    i++;
}
```

## `for` loops

A `for` loop is useful for counting. In only one line of code, it allows us to specify an initial value to use, then a condition to decide if the loop should execute, and finally a means to update the value after each iteration of the loop.

The loop below counts three times, from zero to two:

```js
for (let i = 0; i < 3; i++) {
    console.log('I can count to ' + i);
}
```

Let's break this down:
 - `let i = 0` creates a new variable named `i`, which we use as a counter. You can name this variable whatever you want to, but `i` is a commonly used name for a loop counter. We initialize the variable with zero as its value because in most cases, we'll start counting from zero. For example, the first character in a string is at index zero.
 - `i < 3` is a condition that tells the loop whether it should continue running. If the condition evaluates to `true`, then the loop runs, otherwise it does not.
 - `i++` is how we increment the counter so that each time the loop runs, `i` is always `1` higher than it was in the previous iteration.

Loops are often used to process lists of data. We can treat strings as a list of characters and that means we can manipulate individual characters within a string using a loop. To illustrate, let's log some characters one at a time.

```js
const myName = 'John Doe';
for (let i = 0; i < 3; i++) {
    console.log(myName[i]);
}
```

Now try making the loop go backwards, so that the name is spelled out in reverse.

## `break` and `continue`

Sometimes you may want to skip an iteration of a loop in specific circumstances. To do so, use the `continue` keyword.

Let's count from zero to four, but skip three.

```js
for (let i = 0; i < 5; i++) {
    if (i === 3) {
        continue;
    }
    console.log('I can count to ' + i);
}
```

Somtimes you may want to prematurely exit the loop completely, instead of just skipping an iteration. In that case, use the `break` keyword.

Let's count from zero to four, but abruptly stop counting after two.

```js
for (let i = 0; i < 5; i++) {
    if (i === 3) {
        break;
    }
    console.log('I can count to ' + i);
}
```
