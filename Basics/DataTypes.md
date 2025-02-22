# JavaScript Data Types

JavaScript has 8 data types that can be divided into two categories:
1. Primitive Data Types
2. Non-Primitive (Reference) Data Types

## 1. Primitive Data Types

### 1.1 Number
```javascript
let age = 25;              // Integer
let price = 99.99;         // Float
let infinity = Infinity;   // Special number value
let notANumber = NaN;      // Result of invalid calculations
```

### 1.2 String
```javascript
let firstName = "John";         // Double quotes
let lastName = 'Doe';          // Single quotes
let message = `Hello ${firstName}`; // Template literal
```

### 1.3 Boolean
```javascript
let isActive = true;
let isLoggedIn = false;
```

### 1.4 Undefined
```javascript
let undefinedVariable;
console.log(undefinedVariable); // Output: undefined
```

### 1.5 Null
```javascript
let emptyValue = null;
```

### 1.6 Symbol
```javascript
let sym1 = Symbol();
let sym2 = Symbol("description");
```

### 1.7 BigInt
```javascript
let bigNumber = 9007199254740991n;
let anotherBigNumber = BigInt(9007199254740991);
```

## 2. Non-Primitive Data Types

### 2.1 Object
```javascript
let person = {
    name: "John",
    age: 30,
    isEmployee: true
};

// Accessing object properties
console.log(person.name);      // Dot notation
console.log(person["age"]);    // Bracket notation
```

### 2.2 Array
```javascript
let fruits = ["apple", "banana", "orange"];
let mixed = [1, "hello", true, null, { key: "value" }];

// Accessing array elements
console.log(fruits[0]);    // Output: "apple"
```

### 2.3 Function
```javascript
// Function declaration
function greet(name) {
    return `Hello, ${name}!`;
}

// Function expression
const add = function(a, b) {
    return a + b;
};

// Arrow function
const multiply = (x, y) => x * y;
```

## Type Checking

### Using typeof operator
```javascript
typeof "Hello"         // "string"
typeof 42             // "number"
typeof true           // "boolean"
typeof undefined      // "undefined"
typeof null           // "object" (this is a known JavaScript quirk)
typeof Symbol()       // "symbol"
typeof 42n            // "bigint"
typeof {}            // "object"
typeof []            // "object"
typeof function(){}  // "function"
```

## Type Conversion

### String Conversion
```javascript
String(123)          // "123"
String(true)         // "true"
String(null)         // "null"
String(undefined)    // "undefined"
```

### Number Conversion
```javascript
Number("123")        // 123
Number("12.34")      // 12.34
Number("")           // 0
Number(true)         // 1
Number(false)        // 0
Number(null)         // 0
Number(undefined)    // NaN
```

### Boolean Conversion
```javascript
Boolean("")          // false
Boolean(0)           // false
Boolean(null)        // false
Boolean(undefined)   // false
Boolean(NaN)         // false
Boolean("hello")     // true
Boolean(42)          // true
Boolean({})          // true
Boolean([])          // true
```

## Key Points to Remember

1. JavaScript is a dynamically typed language
2. Primitive types are immutable
3. Reference types are mutable
4. Arrays and Functions are specialized types of Objects
5. Type coercion happens automatically in JavaScript
6. Use strict comparison (`===`) to avoid unexpected type coercion
7. `typeof` is the main operator for type checking

## Best Practices

1. Use strict mode (`'use strict';`) to catch common coding mistakes
2. Always declare variables with `let`, `const`, or `var`
3. Use explicit type conversion when needed
4. Be aware of type coercion in comparisons
5. Use appropriate data types for your data

## Common Pitfalls

1. `null` is of type "object" (JavaScript bug)
2. Array type checking requires `Array.isArray()`
3. NaN is of type "number"
4. All numbers are floating-point internally