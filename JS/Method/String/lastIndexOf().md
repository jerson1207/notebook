# JavaScript String lastIndexOf()
The lastIndexOf() method, given one argument: a substring to search for, searches the entire calling string, and returns the index of the last occurrence of the specified substring. Given a second argument: a number, the method returns the last occurrence of the specified substring at an index less than or equal to the specified number.

### Syntax
```
lastIndexOf(searchString)
lastIndexOf(searchString, position)
```

### Parameters
**searchString**__
- If the method is called with no arguments, searchString is coerced to "undefined". Therefore,"undefined".lastIndexOf() returns 0 — because the substring "undefined" is found at position 0 in the string "undefined". But "undefine".lastIndexOf(), returns -1 — because the substring "undefined" is not found in the string "undefine".

**position**__ Optional
- The method returns the index of the last occurrence of the specified substring at a position less than or equal to position, which defaults to +Infinity. If position is greater than the length of the calling string, the method searches the entire string. If position is less than 0, the behavior is the same as for 0 — that is, the method looks for the specified substring only at index 0.
  - 'hello world hello'.lastIndexOf('world', 4) returns -1 — because, while the substring world does occurs at index 6, that position is not less than or equal to 4.
  - 'hello world hello'.lastIndexOf('hello', 99) returns 12 — because the last occurrence of hello at a position less than or equal to 99 is at position 12.
  - 'hello world hello'.lastIndexOf('hello', 0) and 'hello world hello'.lastIndexOf('hello', -5) both return 0 — because both cause the method to only look for hello at index 0.

### Return Value
The index of the last occurrence of searchString found, or -1 if not found.
### Example
```javascript
const paragraph = 'The quick brown fox jumps over the lazy dog. If the dog barked, was it really lazy?';

const searchTerm = 'dog';

console.log(`The index of the first "${searchTerm}" from the end is ${paragraph.lastIndexOf(searchTerm)}`);
// expected output: "The index of the first "dog" from the end is 52"

```

Strings are zero-indexed: The index of a string's first character is 0, and the index of a string's last character is the length of the string minus 1.
```javascript
'canal'.lastIndexOf('a');     // returns 3
'canal'.lastIndexOf('a', 2);  // returns 1
'canal'.lastIndexOf('a', 0);  // returns -1
'canal'.lastIndexOf('x');     // returns -1
'canal'.lastIndexOf('c', -5); // returns 0
'canal'.lastIndexOf('c', 0);  // returns 0
'canal'.lastIndexOf('');      // returns 5
'canal'.lastIndexOf('', 2);   // returns 2
```
