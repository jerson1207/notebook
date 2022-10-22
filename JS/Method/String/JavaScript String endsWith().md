# JavaScript String endsWith()
The endsWith() method determines whether a string ends with the characters of a specified string, returning true or false as appropriate.
### Syntax
```
endsWith(searchString)
endsWith(searchString, endPosition)
```

### Parameters
**searchString**
- The characters to be searched for at the end of str. Cannot be a regex.


**endPosition** Optional
- The end position at which searchString is expected to be found (the index of searchString's last character plus 1). Defaults to str.length.

### Return Value
**Boolean**
- true if the given characters are found at the end of the string; otherwise, false.

### Example
```javascript
const str = 'To be, or not to be, that is the question.';

console.log(str.endsWith('question.')); // true
console.log(str.endsWith('to be')); // false
console.log(str.endsWith('to be', 19)); // true
```
