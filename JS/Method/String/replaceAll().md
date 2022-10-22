# JavaScript String replaceAll()
returns a new string with all matches of a pattern replaced by a replacement. The pattern can be a string or a RegExp, and the replacement can be a string or a function to be called for each match. The original string is left unchanged.


### Syntax
```
replaceAll(pattern, replacement)
```

#### Parameters
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; pattern
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; replacement

#### Return Value
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; new string - with all matches of a pattern replaced by a replacement.

#### Example
```javascript
'aabbcc'.replaceAll('b', '.');
// 'aa..cc'
```
