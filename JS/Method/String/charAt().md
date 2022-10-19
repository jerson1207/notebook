# JavaScript String charAt()
- The charAt() method returns the character at a specified index (position) in a string.
- The index of the first character is 0, the second 1, ...

### Syntax
```javascript
string.charAt(index)
```
### Parameters
Parameter |	Description
---|---
index	|Optional<br/>The index (position) of the character.<br/>Default = 0.
 
### Return Value
Type	| Description
---|---
String|The character at the specified index.<br/>Empty string ("") if the index is out of range.

## Example
Get the first character in a string:
```javascript
let text = "HELLO WORLD";
let letter = text.charAt(0);
```
> **Note**
> Value of letter is now "H"


Get the last character in a string:
```javascript
let text = "HELLO WORLD";
let letter = text.charAt(text.length-1);
```
> **Note**
> Value of letter is now "D"
