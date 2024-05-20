
---

# JavaScript Cheatsheet

## Basics

### Variables

```javascript
// Declaring variables
var name = 'John'; // var is function-scoped
let age = 25; // let is block-scoped
const pi = 3.14; // const is block-scoped and cannot be reassigned
```

- **var**: Function-scoped. Can be redeclared and updated.
- **let**: Block-scoped. Cannot be redeclared but can be updated.
- **const**: Block-scoped. Cannot be redeclared or updated.

[JavaScript Variables - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#declarations)
[JavaScript Variables - W3Schools](https://www.w3schools.com/js/js_variables.asp)

### Data Types

```javascript
// Primitive data types
let number = 42; // Number
let name = 'Alice'; // String
let isActive = true; // Boolean
let notDefined; // Undefined
let emptyValue = null; // Null
let uniqueId = Symbol('id'); // Symbol
```

- **Number**: Numeric data.
- **String**: Textual data.
- **Boolean**: true or false.
- **Undefined**: A variable declared but not assigned a value.
- **Null**: Represents the intentional absence of any object value.
- **Symbol**: A unique and immutable data type.

[JavaScript Data Types - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures)
[JavaScript Data Types - W3Schools](https://www.w3schools.com/js/js_datatypes.asp)

### Operators

```javascript
// Arithmetic operators
let sum = 5 + 3; // Addition
let difference = 5 - 3; // Subtraction
let product = 5 * 3; // Multiplication
let quotient = 5 / 3; // Division
let remainder = 5 % 3; // Modulus

// Comparison operators
let isEqual = 5 == '5'; // true (loose equality)
let isStrictEqual = 5 === '5'; // false (strict equality)
let isNotEqual = 5 != '5'; // false
let isGreater = 5 > 3; // true
let isLess = 5 < 3; // false

// Logical operators
let andOperator = true && false; // false
let orOperator = true || false; // true
let notOperator = !true; // false
```

- **Arithmetic Operators**: `+`, `-`, `*`, `/`, `%`.
- **Comparison Operators**: `==`, `===`, `!=`, `>`, `<`.
- **Logical Operators**: `&&`, `||`, `!`.

[JavaScript Operators - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators)
[JavaScript Operators - W3Schools](https://www.w3schools.com/js/js_operators.asp)

## Control Structures

### Conditional Statements

```javascript
let number = 10;

if (number > 5) {
    console.log('Number is greater than 5');
} else if (number === 5) {
    console.log('Number is 5');
} else {
    console.log('Number is less than 5');
}
```

- **if**: Executes a block of code if a specified condition is true.
- **else if**: Specifies a new condition to test if the first condition is false.
- **else**: Executes a block of code if the previous conditions are false.

[JavaScript Conditional Statements - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#if...else_statement)
[JavaScript Conditional Statements - W3Schools](https://www.w3schools.com/js/js_if_else.asp)

### Switch Statement

```javascript
let fruit = 'apple';

switch (fruit) {
    case 'apple':
        console.log('It is an apple');
        break;
    case 'banana':
        console.log('It is a banana');
        break;
    default:
        console.log('Unknown fruit');
}
```

- **switch**: Evaluates an expression, matching the expression's value to a case clause, and executes statements associated with that case.

[JavaScript Switch Statement - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/switch)
[JavaScript Switch Statement - W3Schools](https://www.w3schools.com/js/js_switch.asp)

### Loops

#### for Loop

```javascript
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```

- **for**: Creates a loop that is executed as long as a specified condition is true.

#### while Loop

```javascript
let i = 0;

while (i < 5) {
    console.log(i);
    i++;
}
```

- **while**: Creates a loop that executes as long as a specified condition is true.

#### do...while Loop

```javascript
let i = 0;

do {
    console.log(i);
    i++;
} while (i < 5);
```

- **do...while**: Creates a loop that executes at least once and then repeats as long as a specified condition is true.

[JavaScript Loops - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration)
[JavaScript Loops - W3Schools](https://www.w3schools.com/js/js_loop_for.asp)

## Functions

### Function Declaration

```javascript
function greet(name) {
    return 'Hello ' + name;
}

console.log(greet('Alice'));
```

### Function Expression

```javascript
const greet = function(name) {
    return 'Hello ' + name;
};

console.log(greet('Bob'));
```

### Arrow Function

```javascript
const greet = (name) => 'Hello ' + name;

console.log(greet('Charlie'));
```

- **Function Declaration**: Defines a function with the specified parameters.
- **Function Expression**: Creates a function and assigns it to a variable.
- **Arrow Function**: Provides a shorter syntax for writing function expressions.

[JavaScript Functions - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)
[JavaScript Functions - W3Schools](https://www.w3schools.com/js/js_functions.asp)

## Objects and Arrays

### Objects

```javascript
let person = {
    firstName: 'John',
    lastName: 'Doe',
    age: 30,
    greet: function() {
        return 'Hello ' + this.firstName;
    }
};

console.log(person.firstName); // Accessing property
console.log(person.greet()); // Calling method
```

- **Objects**: Collections of key-value pairs.

[JavaScript Objects - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)
[JavaScript Objects - W3Schools](https://www.w3schools.com/js/js_objects.asp)

### Arrays

```javascript
let colors = ['red', 'green', 'blue'];

console.log(colors[0]); // Accessing array element

colors.push('yellow'); // Adding an element
console.log(colors);

colors.pop(); // Removing the last element
console.log(colors);
```

- **Arrays**: Ordered collections of values.

[JavaScript Arrays - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
[JavaScript Arrays - W3Schools](https://www.w3schools.com/js/js_arrays.asp)



### Array Methods

#### forEach

```javascript
const numbers = [1, 2, 3, 4, 5];

numbers.forEach(number => {
    console.log(number);
});
// Logs each number in the array
```

- **forEach**: Executes a provided function once for each array element.

#### map

```javascript
const numbers = [1, 2, 3, 4, 5];
const squaredNumbers = numbers.map(number => number * number);

console.log(squaredNumbers); // [1, 4, 9, 16, 25]
```

- **map**: Creates a new array populated with the results of calling a provided function on every element.

#### reduce

```javascript
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((accumulator, currentValue) => accumulator + currentValue, 0);

console.log(sum); // 15
```

- **reduce**: Executes a reducer function on each element, resulting in a single output value.

#### filter

```javascript
const numbers = [1, 2, 3, 4, 5];
const evenNumbers = numbers.filter(number => number % 2 === 0);

console.log(evenNumbers); // [2, 4]
```

- **filter**: Creates a new array with all elements that pass the test implemented by the provided function.

#### find

```javascript
const numbers = [1, 2, 3, 4, 5];
const firstEvenNumber = numbers.find(number => number % 2 === 0);

console.log(firstEvenNumber); // 2
```

- **find**: Returns the value of the first element that satisfies the provided testing function.

#### findIndex

```javascript
const numbers = [1, 2, 3, 4, 5];
const firstEvenIndex = numbers.findIndex(number => number % 2 === 0);

console.log(firstEvenIndex); // 1
```

- **findIndex**: Returns the index of the first element that satisfies the provided testing function.

[JavaScript Array Methods - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
[JavaScript Array Methods - W3Schools](https://www.w3schools.com/js/js_array_methods.asp)

### Destructuring

#### Array Destructuring

```javascript
const [first, second, ...rest] = [1, 2, 3, 4, 5];

console.log(first); // 1
console.log(second); // 2
console.log(rest); // [3, 4, 5]
```

#### Object Destructuring

```javascript
const person = { firstName: 'John', lastName: 'Doe', age: 30 };
const { firstName, lastName, age } = person;

console.log(firstName); // John
console.log(lastName); // Doe
console.log(age); // 30
```

- **Destructuring**: A syntax that allows unpacking values from arrays or properties from objects into distinct variables.

[JavaScript Destructuring - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)
[JavaScript Destructuring - W3Schools](https://www.w3schools.com/js/js_destructuring.asp)

### Spread Operator

```javascript
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const combined = [...arr1, ...arr2];

console.log(combined); // [1, 2, 3, 4, 5, 6]
```

- **Spread Operator**: Allows an iterable (like an array) to be expanded in places where zero or more arguments or elements are expected.

[JavaScript Spread Operator - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)
[JavaScript Spread Operator - W3Schools](https://www.w3schools.com/js/js_es6.asp#spread)

### Sets

```javascript
const set = new Set([1, 2, 3, 4, 5, 5]);

console.log(set.has(1)); // true
console.log(set.size); // 5
set.add(6);
set.delete(2);
console.log([...set]); // [1, 3, 4, 5, 6]
```

- **Set**: A collection of values where each value must be unique.

[JavaScript Sets - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)
[JavaScript Sets - W3Schools](https://www.w3schools.com/js/js_es6.asp#sets)

### Maps

```javascript
const map = new Map();

map.set('name', 'John');
map.set('age', 30);

console.log(map.get('name')); // John
console.log(map.has('age')); // true
console.log(map.size); // 2
map.delete('name');
console.log(map); // Map(1) { 'age' => 30 }
```

- **Map**: A collection of keyed data items, just like an Object. But unlike an Object, a Map's keys can be any value (including functions, objects, or any primitive).

[JavaScript Maps - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)
[JavaScript Maps - W3Schools](https://www.w3schools.com/js/js_es6.asp#map)

### Entries

```javascript
const arr = ['a', 'b', 'c'];
const entries = arr.entries();

for (let entry of entries) {
    console.log(entry);
}
// Logs [0, 'a'], [1, 'b'], [2, 'c']
```

- **entries**: Returns a new Array Iterator object that contains the key/value pairs for each index in the array.

[JavaScript Array.entries() - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/entries)
[JavaScript Array.entries() - W3Schools](https://www.w3schools.com/jsref/jsref_entries.asp)

## Functions

### Destructuring with Functions

```javascript
function printName({ firstName, lastName }) {
    console.log(`Hello, ${firstName} ${lastName}`);
}

const person = { firstName: 'John', lastName: 'Doe' };
printName(person);
```

### Rest Parameters

```javascript
function sum(...numbers) {
    return numbers.reduce((acc, number) => acc + number, 0);
}

console.log(sum(1, 2, 3, 4)); // 10
```

- **Rest Parameters**: Allows a function to accept an indefinite number of arguments as an array.

[JavaScript Functions - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)
[JavaScript Functions - W3Schools](https://www.w3schools.com/js/js_function_parameters.asp)

## Object-Oriented Programming

### this

```javascript
const person = {
    name: 'John',
    greet() {
        console.log(`Hello, my name is ${this.name}`);
    }
};

person.greet(); // Hello, my name is John
```

- **this**: Refers to the object it belongs to.

[JavaScript this - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)
[JavaScript this - W3Schools](https://www.w3schools.com/js/js_this.asp)

### Prototype Inheritance

```javascript
function Person(name) {
    this.name = name;
}

Person.prototype.greet = function() {
    console.log(`Hello, my name is ${this.name}`);
};

const john = new Person('John');
john.greet(); // Hello, my name is John
```

- **Prototype**: Each function includes a prototype object that is used to implement inheritance and shared properties.

[JavaScript Prototypes - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
[JavaScript Prototypes - W3Schools](https://www.w3schools.com/js/js_object_prototypes.asp)

### Classes

```javascript
class Person {
    constructor(name) {
        this.name = name;
    }

    greet() {
        console.log(`Hello, my name is ${this.name}`);
    }
}

const john = new Person('John');
john.greet(); // Hello, my name is John
```

- **Classes**: Syntactical sugar over JavaScript's existing prototype-based inheritance.

[JavaScript Classes - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
[JavaScript Classes - W3Schools](https://www.w3schools.com/js/js_classes.asp)

### Methods

```javascript
class Person {
    constructor(name) {
        this.name = name;
    }

    greet() {
        console.log(`Hello, my name is ${this.name}`);
    }

    static welcome() {
        console.log('Welcome!');
    }
}

const john = new Person('John');
john.greet(); // Hello, my name is John
Person.welcome(); // Welcome!
```

- **Methods**: Functions defined within a class.

[JavaScript Methods - MDN](https://developer.mozilla.org/en

-US/docs/Web/JavaScript/Reference/Functions)
[JavaScript Methods - W3Schools](https://www.w3schools.com/js/js_object_methods.asp)

## Promises and Asynchronous Programming

### Promises

```javascript
const promise = new Promise((resolve, reject) => {
    setTimeout(() => {
        resolve('Success!');
    }, 1000);
});

promise.then(result => {
    console.log(result); // Success!
}).catch(error => {
    console.error(error);
});
```

- **Promises**: Represent the eventual completion (or failure) of an asynchronous operation and its resulting value.

[JavaScript Promises - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises)
[JavaScript Promises - W3Schools](https://www.w3schools.com/js/js_promise.asp)

### async/await

```javascript
async function fetchData() {
    try {
        let response = await fetch('https://api.example.com/data');
        let data = await response.json();
        console.log(data);
    } catch (error) {
        console.error(error);
    }
}

fetchData();
```

- **async/await**: Syntactic sugar over promises, making asynchronous code easier to write and read.

[JavaScript async/await - MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Async_await)
[JavaScript async/await - W3Schools](https://www.w3schools.com/js/js_async.asp)

## Optional Chaining

```javascript
const user = { address: { city: 'New York' } };
console.log(user?.address?.city); // New York
console.log(user?.address?.street); // undefined
```

- **Optional Chaining (`?.`)**: Allows safe access to deeply nested object properties.

[JavaScript Optional Chaining - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Optional_chaining)
[JavaScript Optional Chaining - W3Schools](https://www.w3schools.com/js/js_optional_chaining.asp)

---
