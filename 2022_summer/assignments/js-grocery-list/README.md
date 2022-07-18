# JavaScript Grocery List

## Description
Practice working with JavaScript loops by building a grocery command line grocery list app.


## Objectives

After completing this assignment, you should…

* understand how to use javascript loops and arrays

## Assignment

Our grocery list script, called `groceries.js`, will allow us to do one of three actions:

1. **Add** an item to our grocery list
2. **Show** our current grocery list
3. **Quit**

Let's tackle each one of these features one by one. But first...

### Getting started with a while loop

A do/while loop is a great tool for repeating something an unknown number of times. In our case, each
time we prompt the user of `groceries.js` to perform an action (**add**, **show** or **quit**) we 
will need to perform that action. Unfortunately we don't know how many items will be added to the 
grocery list or how many times the user will want to show the list. If we knew that they were going 
to add exactly 3 items and then show the list once and then quit we could use a for loop to repeat
our prompt 5 times (3 **adds** + 1 **show** + 1 **quit**). But what if they choose to add 4 items?
This is the perfect opportunity to use a do/while loop:

```js
const prompt = require('prompt-sync')();
let answer;
do {
    answer = prompt('Would you like to "add", "show" or "quit"?');
} while(answer !== 'quit');
```