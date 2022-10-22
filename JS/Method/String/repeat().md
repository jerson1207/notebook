# JavaScript String repeat()
The repeat() method constructs and returns a new string which contains the specified number of copies of the string on which it was called, concatenated together.

### Syntax
```
repeat(count)
```

#### Parameters
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; count - An integer between 0 and +Infinity, indicating the number of times to repeat the string.


### Return Value
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; A new string containing the specified number of copies of the given string.

### Example
```javascript
'abc'.repeat(-1)    // RangeError
'abc'.repeat(0)     // ''
'abc'.repeat(1)     // 'abc'
'abc'.repeat(2)     // 'abcabc'
'abc'.repeat(3.5)   // 'abcabcabc' (count will be converted to integer)
'abc'.repeat(1/0)   // RangeError

({ toString: () => 'abc', repeat: String.prototype.repeat }).repeat(2)
// 'abcabc' (repeat() is a generic method)
```
