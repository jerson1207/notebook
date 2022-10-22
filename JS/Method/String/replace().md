# JavaScript String replace()
The replace() method returns a new string with one, some, or all matches of a pattern replaced by a replacement. The pattern can be a string or a RegExp, and the replacement can be a string or a function called for each match. If pattern is a string, only the first occurrence will be replaced. The original string is left unchanged.

### Syntax
```
replace(pattern, replacement)
```

#### Parameters
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; pattern - Can be a string or an object with a Symbol.replace method — the typical example being a regular expression. Any value that doesn't have the Symbol.replace method will be coerced to a string.
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; replacement - Can be a string or a function.

#### Return Value
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; new string - with one, some, or all matches of the pattern replaced by the specified replacement.

#### Example
```javascript
"xxx".replace("", "_"); // "_xxx"
```
```javascript
function replacer(match, p1, p2, p3, offset, string) {
  // p1 is non-digits, p2 digits, and p3 non-alphanumerics
  return [p1, p2, p3].join(' - ');
}
const newString = 'abc12345#$*%'.replace(/([^\d]*)(\d*)([^\w]*)/, replacer);
console.log(newString);  // abc - 12345 - #$*%
```
