# Javascript String The concat()
The concat() method concatenates the string arguments to the calling string and returns a new string.
### Syntax
```
concat(str1)
concat(str1, str2)
concat(str1, str2, /* …, */ strN)
```

### Parameters
strN
- One or more strings to concatenate to str.

### Return value
A new string containing the combined text of the strings provided.

### Example
```javascript
const greetList = ['Hello', ' ', 'Venkat', '!'];
"".concat(...greetList)
// "Hello Venkat!"
```

```javascript
const hello = 'Hello, ';
console.log(hello.concat('Kevin', '. Have a nice day.'));
// Hello, Kevin. Have a nice day.
```
```javascript
"".concat({})    // "[object Object]"
"".concat([])    // ""
"".concat(null)  // "null"
"".concat(true)  // "true"
"".concat(4, 5)  // "45"
```
