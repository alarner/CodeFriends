# JavaScript Grocery List

## Description
Practice working with JavaScript arrays by building a command line grocery list app.


## Objectives

After completing this assignment, you should…

* understand how to use javascript arrays

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
grocery list or how many times the user will want to show the list. We will learn a lot more about loops in the future, but in the mean time please copy and paste the code below into your `groceries.js` file and write code for the **add** and **show** commands by replacing the comment `// your code goes here`. You will need to use your knowledge of arrays to modify the `groceryList` variable.

```js
const prompt = require('prompt-sync')();
let answer;
let groceryList = [];
do {
    answer = prompt('Would you like to "add", "show" or "quit"?');
    // your code goes here
} while(answer !== 'quit');
```

## Bonus

See if you can use [fs.writeFileSync](https://nodejs.org/api/fs.html#fswritefilesyncfile-data-options), [JSON.stringify](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/stringify) and [JSON.parse](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse) to save your grocery list so that
each time you run the `groceries.js` script your list is preserved.