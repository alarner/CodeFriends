# JavaScript Arrays

> To do list:
> 1. Buy a turtle
> 2. Name it 'The speed of light'
> 3. Be able to honestly say I can run faster than the speed of light

### You should already know about
* [JavaScript primitives](../javascript-primitives/README.md)

We've learned about some of the data types in JavaScript (you may remember numbers, strings and booleans). You may have wondered how you can build complex applications like some of the social media apps, google, etc. with just these basic types. Is there a developer somewhere writing a new string variable each time someone writes a tweet? That doesn't sound sustainable. If you use your imagination there are countless things you do on a daily basis that involve ordered lists of things. Maybe you have a to-do list? Your calendar is an ordered list of events. Social media feeds are an ordered list of posts. Even driving in your car involves going from point A to point B to point C.

Arrays are a data type in JavaScript that allows us to **keep track of an ordered lists of entries**. Here the entry could be whatever we want. It's the thing in the list that we are keeping track of (eg. to-do item, calendar event, social media post, etc). Other programming languages also have some form of arrays but they might have a different name. The entries of an array can be any data type in JavaScript (string, boolean, number, etc) and can even be arrays themselves!

> Vocabulary tip: entries are also sometimes called elements or items.

## Array syntax

### Declaring and assigning arrays

We use the square brackets `[]` to denote an array in JavaScript. For example:

```
console.log(['red', 'orange', 'yellow', 'green', 'blue', 'indigo', 'violet']);
const states = ['Alabama', 'Alaska', 'Arizona', 'Arkansas'];
const decades = [1980, 1990, 2000, 2010, 2020];
const answers = [true, false, true, true, true];
const emptyArray = [];
```

These are all different ways of creating arrays.

### Accessing an element of an array

An important part of arrays is that they are **ordered**. When we want to look up a single element of an array we do so by asking for it by its order in the array. Developers call the order the **index**.

```
const states = ['Alabama', 'Alaska', 'Arizona', 'Arkansas'];
console.log(states[2]);
console.log(states[0]);
```

This will display "Arizona" followed by "Alabama". Notice we are using square brackets with the index inside to access a single element of an array.

One thing that takes a while to get used to is that arrays are said to be **zero-indexed**. This means that the first element in an array is at index 0. This means that even though "Arizona" is the third element in the array, its index is 2, not 3, because the array starts at index 0, not 1. Starting at zero turns out to be handy in many cases, but can definitely take some getting used to.

#### indexes as variables

We can also use variables as indexes.

```
const states = ['Alabama', 'Alaska', 'Arizona', 'Arkansas'];
const arkansasIndex = 3;
console.log(states[arkansasIndex]);
```

In the above example `arkansasIndex` evaluates to 3 because we gave it a value of 3 on the second line, so `states[arkansasIndex]` is equivalent to `states[3]`.


### Array methods

It's very easy to manipulate arrays with several different array methods:

Here's an example of adding to an array with [push](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push) and [unshift](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift) methods.

```
const states = ['Alabama', 'Alaska', 'Arizona', 'Arkansas'];
states.push('California'); // Adds 'California' to the end of the array
console.log(states[4]); // outputs 'California'
```

```
const states = ['Alabama', 'Alaska', 'Arizona', 'Arkansas'];
states.unshift('California'); // Adds 'California' to the beginning of the array
console.log(states[0]); // outputs 'California'
```

Here are some other handy array manipulation methods:

> No need to memorize everything about these, but it is important to know that they exist so that you can look them up when you need to use them.

* [concat](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat) - join two or more arrays together.
* [includes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/includes) - determines whether an array includes a certain value among its entries.
* [join](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join) - creates and returns a new string by combining (concatenating) all of the elements in an array.
* [pop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop) - removes the last element from an array and returns that element.
* [reverse](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift) - reverses the order of the array.
* [shift](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift) - removes the first element from an array and returns that removed element
* [slice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice) - returns a copy of a portion of the array.
* [splice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice) - changes the contents of an array by removing or replacing existing elements and/or adding new elements.