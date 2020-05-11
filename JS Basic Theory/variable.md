# JS Variables

> Variables are named values and can store any type of JavaScript value.

Here’s how to declare a variable:

*EXAMPLE*

`var x = 100`;

And here’s what’s happening in the example above:

- var is the **keyword** that tells JavaScript you’re declaring a variable.
- x is the **name** of that variable.
- = is the **operator** that tells JavaScript a value is coming up next.
- 100 is the **value** for the variable to store.
___ 
## Using variables

+ After you declare a variable, you can reference it by name elsewhere in your code.

*EXAMPLE*

var x = 100;
x + 102;

*OUTPUT*:-`202`

+ You can even use a variable when declaring other variables.

*EXAMPLE*

var x = 100;
var y = x + 102;
y;

*OUTPUT*:-`202`
___
## Reassigning variables

+ You can give an existing variable a new value at any point after it’s declared.

*EXAMPLE*

var weather = "rainy";
​weather = "sunny";
weather;

*OUTPUT*:-`"sunny"`
___
## Naming variables

Variable names are pretty flexible as long as you follow a few rules:

- Start them with a letter, underscore _, or dollar sign $.
- After the first letter, you can use numbers, as well as letters, underscores, or dollar signs.
- Don’t use any of JavaScript’s reserved keywords.

> With that in mind, here are valid variable names:

*EXAMPLE*

var camelCase = "lowercase word, then uppercase";
var dinner2Go = "pizza";
var I_AM_HUNGRY = true;
var _Hello_ = "what a nice greeting"
var $_$ = "money eyes";

> here are some invalid variable names — try to spot what’s wrong with each of them:

*EXAMPLE*

var total% = 78;
var 2fast2catch = "bold claim";
var function = false;
var class = "easy";

Variable names are case-sensitive, so myVar, MyVar, and myvar are all different variables. But generally,
it’s a good practice to avoid naming variables so similarly.