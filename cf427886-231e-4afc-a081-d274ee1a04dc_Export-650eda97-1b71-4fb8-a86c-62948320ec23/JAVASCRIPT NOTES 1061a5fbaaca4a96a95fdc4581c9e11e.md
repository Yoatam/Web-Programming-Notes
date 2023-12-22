# JAVASCRIPT NOTES

## Node.js

is a runtime environment used to run JavaScript on machine.

## Data Types

      **1. Primitive datatypes**

- numbers: `int` and `float`
- bool: `true` or `false`
- string: uses single quote by convention

```cpp
x = 12
```

| x |  |
| --- | --- |
| 12 |  |
| 004 |  |

```cpp
y = x
```

| x | y |
| --- | --- |
| 12 | 12 |
| 004 | 005 |

```cpp
x = 6
```

| x | y |
| --- | --- |
| 6 | 12 |
| 004 | 005 |

       

            **2. Non primitive datatypes**

AKA reference data types 

- Class
- String
- Array
- Interface

```cpp
names = {'Hanna', 'Abel'}
```

| names |  |
| --- | --- |
| 101 |  |

| Hanna | Abel |
| --- | --- |
| 101 | 101 |
| 004 | 005 |

## Variable declaration

### **Automatically**

```jsx
x = 5;
y = 6;
z = x + y;
```

### Using `var`

The `var` keyword should only be used in code written for older browsers.

```jsx
var x = 5;
var y = 6;
var z = x + y;
```

### Using `let`

```jsx
let firstname = 'Hallan'
```

### Using `const`

used to declare constant variables. These values and cannot be changed.

```jsx
const firstName = 'Hallan'
const PI = 3.14 //by convention capital letters are used for const
```

## Operators

### Assignment operators

| Operator | Description |
| --- | --- |
| + | Addition |
| - | Subtraction |
| * | Multiplication |
| ** | Exponentiation (https://www.w3schools.com/js/js_2016.asp) |
| / | Division |
| % | Modulus (Division Remainder) |
| ++ | Increment |
| -- | Decrement |

### Ternary operator

```jsx
//output: underage
let age = 17
let adult = (age >= 18) ? 'adult' : 'underage'
console.log(adult)
```

 

## Arrays

a special variable, which can hold more than one value:

```jsx
const arr1 =[23, 4, 23, 4, 324, , 324, 3, 5]

console.log(arr1[6])
```

## Functions

- Function with no return value
    
    ```jsx
    //output: Hello
    function greet()
    {
    	console.log('Hello')
    }
    
    greet()
    ```
    

- Function with return value
    
    ```jsx
    //output: Hello
    function greet()
    {
    	return 'Hello'
    }
    console.log(greet())
    ```
    

- Anonymous function
    
    ```jsx
    //output: Hello Hanna
    let firstName = 'Hanna'
    
    let func = function(name)
    {
    	return 'Hello ' + name
    }
    console.log(func(firstName))
    ```
    

- Arrow function
    
    ```jsx
    /*output: 
    Hello World!
    Hello World!
    */
    hello = () => {
      return "Hello World!";
    }
    console.log(hello)
    
    hello2 = () => "Hello World!";
    console.log(hello2)
    
    fName = 'Abebe'
    hello3 = (val) => "Hello " + val;
    console.log(hello3(fName))
    ```
    
    If we have only one parameter, you can skip the parentheses as well
    
    ```jsx
    //output: 30
    let a = 10
    let b = 3
    
    let myFunction = (a, b) => a * b;
    
    console.log(myFunction(a, b))
    ```