# JavaScript String matchAll()
The matchAll() method returns an iterator of all results matching a string against a regular expression, including capturing groups.

### Syntax
```
matchAll(regexp)
```

### Parameters
regexp

### Return Value
an array with the same shape as the return value of RegExp.prototype.exec().

### Example
The matchAll() method returns an iterator of results after matching a string against a regular expression.
```javascript
// string definition
const sentence = "JavaScript1JavaScript2";

// a pattern having 'JavaScript' followed by a digit
const regex = /JavaScript\d/g;

// finding matches in the string for the given regular expression
let results = sentence.matchAll(regex);

// looping through the iterator
for (result of results) {
  console.log(result);
}

// Output:
// ["JavaScript1", index: 0, input: "JavaScript1JavaScript2", groups: undefined]
// ["JavaScript2", index: 11, input: "JavaScript1JavaScript2", groups: undefined]
```
