# JavaScript String includes()
- The includes() method performs a case-sensitive search to determine whether one string may be found within another string, returning true or false as appropriate.
- This method lets you determine whether or not a string includes another string.
- Case sensitive

### Syntax
```
includes(searchString)
includes(searchString, position)
```
**position** Optional
- The position within the string at which to begin searching for searchString. (Defaults to 0.)
### Parameters

**searchString**
- A string to be searched for within str. Cannot be a regex.


### Return Value
**Boolean**
- true if the search string is found anywhere within the given string; otherwise, false if not.

### Example
```javascript
const sentence = 'The quick brown fox jumps over the lazy dog.';

const word = 'fox';

console.log(`The word "${word}" ${sentence.includes(word) ? 'is' : 'is not'} in the sentence`);
// expected output: "The word "fox" is in the sentence"
```
