[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/1MjEPKdA)
# Higher Order Functions

## Learning Goals

- [ ] **Recall the benefits of higher-order functions.**
- [ ] **Write a callback and higher-order function.**
- [ ] **Pass a higher-order function a callback.**
- [ ] **Use the built-in higher-order function `map` to “transform” items in an array and return a new array.**
- [ ] **Use the built-in higher-order function `filter` to “filter” values from an array and return a new array.**

## Higher-Order Functions in JavaScript

Higher-order functions are a huge part of developing with JavaScript. In this lab, you will be implementing a higher-order function and using built-in JavaScript higher-order functions.

### Functions as Values

In JavaScript, functions are values that can be assigned to variables. Because of this, we can pass functions as parameters to other functions.

- Callback Function: A function passed as an argument to another function is called a callback function.
- Higher-Order Function: A function that receives a function as an argument and/or returns a function is called a higher-order function.

```
const foo = function() {
  console.log("I’m a function!");
};

const boo = function(callback) {
  console.log("Higher Order");
  return callback();
};

boo(foo);
```

## Arrow Functions

In this lab, we will be using arrow functions. If you are unfamiliar with arrow functions, you can learn more by checking out the following resources:

- [Arrow Functions Documentation on W3Schools](https://www.w3schools.com/js/js_arrow_function.asp)
- [Arrow Functions Video Tutorial](https://www.youtube.com/watch?v=fRRRkognpOs)

## Lab Deliverables

1. Build a higher order function

- Create a function called `callback` that `console.log`s the message "Callback Function".
- Create a function called `higherOrder` that takes a parameter called `foo`. Inside the `higherOrder` function, `console.log` the message "Higher Order Function", and then invoke `foo()` by returning it.

<details>
  <summary>Click Here to view solution</summary>

```

// 1. Introduction to Higher Order Functions
// Callback function definition
const callback = () => {
  console.log("Callback Function");
};

// Higher Order Function definition
const higherOrder = (foo) => {
console.log("Higher Order Function");
return foo(); // Execute the callback function
};
```

</details>

2. Use JavaScript Built in Higher Order Function Map

- Create a variable called `uppercaseMenu` and set it to `brunchMenu.map`.
- Inside the parentheses `()`, write an anonymous arrow function that takes a parameter `menuItem` and returns `menuItem.toUpperCase()`.

- Log `uppercaseMenu` to the console and view it to confirm that a new array was created where the brunch menu items are transformed to uppercase.

<details>
  <summary>Click Here to view solution</summary>

```
// Map - "Transforms" each item in the array and returns a new array

const uppercaseMenu = brunchMenu.map((menuItem) => menuItem.toUpperCase());
console.log(uppercaseMenu);

// ["EGGS BENEDICT", "HUEVOS RANCHEROS", "FRIED CHICKEN & WAFFLE", "FRIED EGG SANDWICH"]


```

</details>

3. Use JavaScript Built in Higher Order Function Filter

- Create a variable called `cheaperMenuPrices` and set it to `brunchPrices.filter`.

- Inside the parentheses `()`, write an anonymous arrow function that takes a parameter `price` and returns `true` if the `price` is under 17.

- Log `cheaperMenuPrices` to the console and view it to confirm that a new array was created with every price under 17.

<details>
  <summary>Click Here to view solution</summary>

```
// Filter - Returns a new array with items that pass the condition in the callback

const cheaperMenuPrices = brunchPrices.filter((price) => price < 17);
console.log(cheaperMenuPrices);

// [15.0, 16.0, 12.0]


```

</details>

## Submission Instructions

1. Push your code to GitHub.
2. Submit the link to your GitHub repository URL.
