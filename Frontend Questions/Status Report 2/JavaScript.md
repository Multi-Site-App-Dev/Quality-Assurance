# JavaScript

1.What is JavaScript? What do we use it for?

2. Can we run JavaScript in a web browser, on a server, or both?

3. What programming paradigm(s) does JS support?

4. What are the data types in JS?

  * What is the type of NaN? What is the isNaN function?

  * What is the data type of a function?

  * What about an array?

  * What is the difference between undefined and null?

5. What are JS objects? what is the syntax?

6. Use the object literal syntax to create an object with some properties

7. What are arrays in JS? can you change their size?

8. List some array methods and explain how they work.

9. What is JSON? Is it different from JS objects?

10. What are some ways you can use functions in JS?

11. What are the different scopes of variables in JS?

  * What are the different ways to declare global variables?

  * Is it a best practice to use global variables? Why or why not?

12. What are some methods on the function prototype?

13. If you declare a variable `var` inside a for loop is that block scoped or function scoped?

  * If you declare a variable `let` inside a for loop is that block scoped or function scoped?

14. What will happen?

```javascript
const hi;
hi = 3;
console.log(hi);
```

15. What are callback functions? What about self-invoking functions?

16. What is a truthy or falsy value? List the falsy values.

17. What prints?:

```javascript
let x = 5;
while(x) {
  x--;
  console.log(x);
}
```

18 What is the difference between == and ===? Which one allows for type coercion?

19. What is the difference between `for of` and `for in`? Give examples.

20. What does the following code do?

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

19. What is the difference between a do-while and a while loop?

20. What does this do?

```javascript
for(;;){
    console.log('a');
}
```

21. What is fall-through with regard to switch statements?

22. What is the difference between `console.log(++x)` and `console.log(x++)`?

23. Explain what “strict mode” does   

24. What are the naming conventions for a variable used in JavaScript?

25. What are the naming conventions for a function used in JavaScript?
