# JavaScript

## Language Fundamentals

### Basic

* What is JavaScript? What do we use it for?

* Can we run JavaScript in a web browser, on a server, or both?

* What programming paradigm(s) does JS support?

* What are the data types in JS?

  * What is the type of NaN? What is the isNaN function?

  * What is the data type of a function?

  * What about an array?

  * What is the difference between undefined and null?

* What are JS objects? what is the syntax?

* Use the object literal syntax to create an object with some properties

* What are arrays in JS? can you change their size?

* List some array methods and explain how they work.

* What is JSON? Is it different from JS objects?

* What are some ways you can use functions in JS?

* What are the different scopes of variables in JS?

  * What are the different ways to declare global variables?

  * Is it a best practice to use global variables? Why or why not?

* What are some methods on the function prototype?

* If you declare a variable `var` inside a for loop is that block scoped or function scoped?

  * If you declare a variable `let` inside a for loop is that block scoped or function scoped?

* What will happen?

```javascript
const hi;
hi = 3;
console.log(hi);
```

* What are callback functions? What about self-invoking functions?

* What is a truthy or falsy value? List the falsy values.

* What prints?:

```javascript
let x = 5;
while(x) {
  x--;
  console.log(x);
}
```

* What is the difference between == and ===? Which one allows for type coercion?

* What is the difference between `for of` and `for in`? Give examples.

* What does the following code do?

```javascript
function addOne(value) {
    value + 1;
}

let x = 5;
addOne(x);
console.log(x);
```

What about this?

```javascript
function changeUsername(user) {
    user.username = 'new-username';
}

let user = {
    username: 'first-username'
};

changeUsername(user);
console.log(user.username);
```

* What is the difference between a do-while and a while loop?

* What does this do?

```javascript
for(;;){
    console.log('a');
}
```

* What is fall-through with regard to switch statements?

* What is the difference between `console.log(++x)` and `console.log(x++)`?

* Explain what “strict mode” does   

* What are the naming conventions for a variable used in JavaScript?

* What are the naming conventions for a function used in JavaScript?
