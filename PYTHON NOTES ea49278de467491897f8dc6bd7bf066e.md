# PYTHON NOTES

# Variable Declaration

 It doesn’t need datatype specification

```python
a = 5
a = True
a = 'char'
```

to find the datatype of a variable we can use `type` method

```python
print(type(a))
output = #<class, 'str'
```

### List

A list is a collection of elements which is ordered and mutable. Lists are defined using square brackets **`[]`**.

```python
names = ["John", "Bob", "Katy", "Mosh"]
print(names[0]) #John
names[0] = "Jon"
print(names[0]) #Jon

```

List object methods

```python
numbers = [1, 2, 3, 4, ,5]

#to add new entry/element at the end
numbers.append(6)
print(numbers) #[1, 2, 3, 4, ,5, 6]

#to add new entry/element at a specific index
numbers.insert(-1, 6) #(index, element)
print(numbers) #[1, 2, 3, 4, ,5 , 6]

#to remove an element
numbers.remove(1)
print(numbers) #[2, 3, 4, ,5, 6]

#to remove all elements
numbers.clear()
print(numbers) #[]

#to check for an elements
print(1 in numbers) #False

#to find number of elements
print(numbers.len()) #5

```

### Tuples

A tuple is similar to a list but is immutable, meaning you cannot change its elements after it's created. Tuples are defined using parentheses **`()`**.

```python
numbers = (1, 2, 3)
numbers[0] = 4 #error
```

  there are only two methods `.count()` and `.index()`

```python
# count the number of occurences of an element
numbers = (1, 2, 3, 4)
print(numbers.count(3)) #2

#find an element and return the index
numbers = (1, 2, 3, 4)
print(numbers.index(3)) #2
```

### Set

A set is an unordered collection of unique elements. Sets are defined using curly braces **`{}`**.

```python
names = {"John", "Bob", "Katy", "Mosh"}
print(names[0]) #John

```

### **Dictionary**

A dictionary is a collection of key-value pairs. It is unordered, mutable, and each key in a dictionary must be unique. Dictionaries are defined using curly braces **`{}`** and key-value pairs separated by colons **`:`**.

```python
studentInfo = {
	'name': 'hanna', 'age': 12, 'sec': 'B','height': 1.5, 
	'skills': ['java', 'javaScript', 'python']

print(studentInfo['height'])
#output = 1.5
```

## Flow control

### For loop

A for loop is used for iterating over a sequence (such as a list, tuple, set, or dictionary) or other iterable objects. It executes a block of code repeatedly until the sequence is exhausted.

```python
numbers = [1, 2, 3, 4, ,5]

for item in numbers:
	print(item)
#1
#2
#3
#4
#5
```

### **Range function**

 It generates a sequence of numbers and returns an object

```python
for item in range(1, 6):
	print(item)
#1
#2
#3
#4
#5
```

```python
#to have both index and values we can use enumerate()
names = {"John", "Bob", "Katy", "Mosh"}
for index, value in enumerate(names):
	print(str(index) + ' ' + str(value))
```

### If-else

Certainly! In Python, the **`if`**, **`elif`** (else if), and **`else`** statements are used for conditional execution of code. Here's the basic syntax:

```python
if condition1:
    # code block to execute if condition1 is True
elif condition2:
    # code block to execute if condition1 is False and condition2 is True
else:
    # code block to execute if both condition1 and condition2 are False

```

Here's an example:

```python

weight = float(input("Enter weight: "))
unit = input("(K)g or (L)bs: ")
if unit.upper() == "K":
    weight *= 2.204
    print(weight)
elif unit.upper():
    weight /= 2.204
    print(weight)
else:
    print("Invalid unit")
```

## Function

A function is a block of reusable code that performs a specific task. In Python, we can define our own functions using the `def` keyword.

In the example, we have defined two functions. The `greet()` function simply prints "hello world!". The `greetWithName()` function takes three parameters: `name`, `age`, and an optional parameter `lastName`. It then prints a customized greeting message using the provided parameters.

To call a function, we simply write the function name followed by parentheses. If the function takes parameters, we pass them inside the parentheses.

```python
def greet():
	print('hello world!')
	
def greetWithName(name, age, lastName = 'kebede'):
 print(f'Hello {name} age:{age} Last Name: {lastName} ')
		
greet()
greetWithName('hanna', age=56)

#output
hello world!
Hello hanna age:56 Last Name: kebede
```

  

## Argument Types

**Positional Argument**

A positional argument is an argument that is passed to a function based on its position or order in the function call. 

```python
greet('hanna', 56) 
```

**Keyword Argument**

By using keyword arguments, we can explicitly specify which parameter corresponds to which argument, making our code more readable and self-explanatory.

```python
greet(age = 56)

```

**Default Argument**

A default argument is a parameter that has a default value specified in the function definition. If the argument is not provided when calling the function, the default value will be used.

```python
def greet(name, age=30):
    print(f"Hello {name}, you are {age} years old.")

greet("John")  # Hello John, you are 30 years old.
greet("Jane", 25)  # Hello Jane, you are 25 years old.

```