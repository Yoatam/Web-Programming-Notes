# Javascript String Methods

# I. Javascript String Length

The `length` property returns the length of a string:

```jsx
let text = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
let length = text.length;
```

# Extracting String Parts

There are 3 methods for extracting a part of a string:

### 1. JavaScript String slice()

`slice()` extracts a part of a string and returns the extracted part in a new string.

The method takes 2 parameters: start position, and end position (end not included).

```jsx
let text = "Apple, Banana, Kiwi";
let part = text.slice(7, 13);
```

If you omit the second parameter, `slice()` will slice out the rest of the string.

### 2. JavaScript String substring()

`substring()` is similar to `slice()`.

The difference is that start and end values less than 0 are treated as 0 in `substring()`.

```jsx
let str = "Apple, Banana, Kiwi";
let part = str.substring(7, 13);
```

If you omit the second parameter, `substring()` will slice out the rest of the string.

### 3. JavaScript String substr()

`substr()` is similar to `slice()`.

The difference is that the second parameter specifies the **length** of the extracted part.

```jsx
let str = "Apple, Banana, Kiwi";
let part = str.substr(7, 6);
```

If you omit the second parameter, `substr()` will slice out the rest of the string.

# II. Replacing String Content

The `replace()` method replaces a specified value with another value in a string:

```jsx
let text = "Please visit Microsoft!";
let newText = text.replace("Microsoft", "W3Schools");
```

The `replace()` method does not change the string it is called on.

The `replace()` method returns a new string.

The `replace()` method replaces **only the first** match.

# III. JavaScript String ReplaceAll()

The `replaceAll()` method allows you to specify a regular expression instead of a string to be replaced.

If the parameter is a regular expression, the global flag (g) must be set, otherwise a TypeError is thrown.

The `replaceAll()` does not work in Internet Explorer.

```jsx
text = text.replaceAll(/Cats/g,"Dogs");
text = text.replaceAll(/cats/g,"dogs");
```

# IV. **JavaScript String toUpperCase()**

A string is converted to upper case with `toUpperCase()`

```jsx

let text1 = "Hello World!";
let text2 = text1.toUpperCase();
```

# V. **JavaScript String toLowerCase()**

A string is converted to lower case with `toLowerCase()`

```jsx
let text1 = "Hello World!";       // String
let text2 = text1.toLowerCase();  // text2 is text1 converted to lower
```

# VI. JavaScript String concat()

`concat()` joins two or more strings.

The `concat()` method can be used instead of the plus operator.

All string methods return a new string. They don't modify the original string.

```jsx
let text1 = "Hello";
let text2 = "World";
let text3 = text1.concat(" ", text2);

text = "Hello" + " " + "World!";
text = "Hello".concat(" ", "World!");
```

# VII. JavaScript String trim()

The `trim()` method removes whitespace from both sides of a string.

```jsx
let text1 = "      Hello World!      ";
let text2 = text1.trim();
```

# VIII. JavaScript String trimStart()

The `trimStart()` method works like `trim()`, but removes whitespace only from the start of a string.

```jsx
let text1 = "     Hello World!     ";
let text2 = text1.trimStart();
```

# IX. JavaScript String trimEnd()

The `trimEnd()` method works like `trim()`, but removes whitespace only from the end of a string.

```jsx
let text1 = "     Hello World!     ";
let text2 = text1.trimEnd();
```

# X. JavaScript String padStart()

The `padStart()` method pads a string from the start.

It pads a string with another string (multiple times) until it reaches a given length.

```jsx
let text = "5";
let padded = text.padStart(4,"0");
```

# XI. JavaScript String padEnd()

The `padEnd()` method pads a string from the end.

It pads a string with another string (multiple times) until it reaches a given length.

```jsx
let text = "5";
let padded = text.padEnd(4,"0");
```

# Extracting String Characters

There are 3 methods for extracting string characters:

### 1. JavaScript String charAt()

The `charAt()` method returns the character at a specified index (position) in a string:

```jsx
let text = "HELLO WORLD";
let char = text.charAt(0);
```

### 2. JavaScript String charCodeAt()

The `charCodeAt()` method returns the unicode of the character at a specified index in a string.

The method returns an integer between 0 and 65535.

```jsx
let text = "HELLO WORLD";
let char = text.charCodeAt(0);
```

### 3. Property Access

It allows property access [ ] on strings:

```jsx
let text = "HELLO WORLD";
let char = text[0];
```

# XII. JavaScript String split()

A string can be converted to an array with the `split()` method:

If the separator is omitted, the returned array will contain the whole string in index [0].

If the separator is "", the returned array will be an array of single characters.

```jsx
text.split(",")    // Split on commas
text.split(" ")    // Split on spaces
text.split("|")    // Split on pipe
```