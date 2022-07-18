# JavaScript Loops

> Pete and Repeat were sitting on a fence. Pete fell off. Who’s left?

### You should already know about
* [JavaScript arrays](../javascript-arrays/README.md)

Loops unlock a whole new world of possibilities in JavaScript (and exist in pretty much every programming language). They allow us to make monotonous repeatating tasks much easier. Sometimes we know that our code needs to do a similar thing 100 times or 1,000 times. If we were writing the instructions to make a peanut butter and jelly sandwich it might look like:

1. Open jar of peanut butter
2. Open jar of jelly
3. Take slice of bread `a` from loaf and lay flat
4. Spread peanut butter on top face of bread `a`
5. Take slice of bread `b` from loaf and lay flat
6. Spread jelly on top face of bread `b`
7. Place peanut butter face of bread `a` on top of jelly face of bread `b`
8. Place sandwich aside

If we wanted to make 1,000 peanut butter and jelly sandwiches we will at lease need to repeat steps three to eight 1,000 times. That's a lot of steps!

As you've learned, writing code is like writing a series of steps that the interpreter can understand. If we wanted to write code to do the same thing many times we don't want to have to copy any paste steps. Not only does this make our code *super long*, but it also makes it hard to change any one of the steps because we have to change it in many different places. This is where loops come in. They essentially allow us to tell the computer to repeat one or more steps more than once.

## Different types of loops

There are several different types of loops that are useful in different scenarios.

### `while` loops

`while` loops are the tool of choice if we don't know how many times we want to repeat a task. For example:

```
let answer;
while(answer != "42") {
    answer = prompt(`What is the meaning of life the universe and everything?`);
}
```
This while loop will ask the user: "What is the meaning of life the universe and everything?" until they answer "42." It will just keep going until the answer is the string `42`. This is a scenario where we need to repeat a task an unknown number of times because we don't know how many times it will take the user until they answer `42`.

A while loop is very similar to an if statement in that it will evaluate the expression inside the parentheses and run the code in the brackets if it evaluates to true. The difference is that the while loop will keep repeating until the expression evaluates to false.

### `do ... while` loops

`do ... while` loops are very similar to while loops except they run the code first and *then* check the expression. Writing the same code as above, but with a `do ... while` loop would look like this:

```
let answer;
do {
    answer = prompt(`What is the meaning of life the universe and everything?`);
} while(answer != "42");
```

#### Be careful of infinite loops!

Since `while` loops and `do ... while` don't have a finite stopping point, it's possible for them to run forever if the expression in parentheses always evaluates to `true`. For example:

```
do {
    console.log("Pete and Repeat were sitting on a fence. Pete fell off. Who’s left?");
    console.log("Repeat");
} while(true);
```

Inifinite loops will keep going until you force them to stop with `ctrl`+`c` or your computer runs out of batteries!

### `for` loops

`for` loops are one of the most common type of loops. They are used to repeat a task a fixed number of times.

```
for(let fancyNumber = 0; `fancyNumber < 4; fancyNumber = fancyNumber + 1) {
    console.log(fancyNumber);
}
```

This code displays the numbers 0, 1, 2, 3, each on their own line. Inside the parentheses of a for loop there are actually three parts. The three parts are separated by `;`. Let's look at them one by one...

for(`let fancyNumber = 0;` `fancyNumber < 4;` `fancyNumber = fancyNumber + 1`)

#### Part 1: initialization

```
let fancyNumber = 0;
```

The first part is called the initialization. It tells the loop **where to start**. In this case we are starting at the number 0, but we could start with any number. Usually this part will include declaration and assignment of a variable to use in the loop.

#### Part 2: condition

```
fancyNumber < 4;
```

The second part is called the condition. It tells the loop **when to continue**. Just like the while loop or if statement, when this expression evaluates to true, the code inside the loop will run. In this case it will keep running until `fancyNumber` is 4. At that point the expression will evaluate to false and will stop running.

> This means that the last number to be displayed will be `3`.
> What do you think would happen if the condition was `fancyNumber <= 4;`?

#### Part 3: increment / decrement

```
fancyNumber = fancyNumber + 1
```

The third part is called the increment / decrement. It tells the loop **how to change**. This code will run each time the code in the for loop runs and it will change the variable that was declared in the initialization part. It's designed to make sure the loop stops at some point, but there are no gaurantees. You need to make sure you write your code in a way that it will eventually stop, otherwise you could run in to an [infinite loop!](#)

Most of the time you will be increasing your variable by 1 each time, but you could increase by any number, or even count backwards by decreasing the variable, eg. `fancyNumber = fancyNumber - 2`.

#### PB&J

This code will write out the steps to make 10 peanut butter and jelly sandwiches. Can you identify the different parts inside the for loop parentheses and what they will do?

```
console.log("Open jar of peanut butter");
console.log("Open jar of jelly");
for(let i = 0; i < 10; i++) {
    console.log("Take slice of bread `a` from loaf and lay flat");
    console.log("Spread peanut butter on top face of bread `a`");
    console.log("Take slice of bread `b` from loaf and lay flat");
    console.log("Spread jelly on top face of bread `b`");
    console.log("Place peanut butter face of bread `a` on top of jelly face of bread `b`");
    console.log("Place sandwich aside");
}
```

### Iterating over arrays

A common task we need to do as developers is to visit each entry in an array and do something with it. This process is called **iterating** over an array. There are many ways to do this using different types of loops, but here I cover two common techniques.

#### using a for loop

```
const colors = ['red', 'orange', 'yellow', 'green', 'blue', 'indigo', 'violet'];

for(let i = 0; i < colors.length; i++) {
    console.log(`My favorite color is ${colors[i]}`);
}
```

In this example we use a for loop to generate each index of the array (stored in the variable `i`) startwith with 0 and going through 6. Then we access the value at each index and display the value inside of a message to the console.

#### using a for ... of loop

The `for ... of` loop is a special loop that's specifically designed for iterating over arrays. It has a clearer and simpler syntax than a for loop, so it's often the preference.

```
const colors = ['red', 'orange', 'yellow', 'green', 'blue', 'indigo', 'violet'];

for(const c of colors) {
    console.log(`My favorite color is ${c}`);
}
```

In this case there are only two parts inside the parentheses.

1. `const c` declares a variable that will hold each value in the array. 
2. `of colors` defines the array that we are iterating over.

Much simpler!