# JavaScript String padStart()
The padStart() method pads the current string with another string (multiple times, if needed) until the resulting string reaches the given length. The padding is applied from the start of the current string.

### Syntax
```
padStart(targetLength)
padStart(targetLength, padString)
```

### Parameters
**_targetLength_** - The length of the resulting string once the current str has been padded. If the value is less than str.length, then str is returned as-is.

**_padString_** (Optional) - The string to pad the current str with. If padString is too long to stay within the targetLength, it will be truncated from the end. The default value is the unicode "space" character (U+0020).

### Return Value
**_String_** - specified targetLength with padString applied from the start.

### Example
Basic examples
```javascript
'abc'.padStart(10);         // "       abc"
'abc'.padStart(10, "foo");  // "foofoofabc"
'abc'.padStart(6,"123465"); // "123abc"
'abc'.padStart(8, "0");     // "00000abc"
'abc'.padStart(1);          // "abc"
```

Fixed width string number conversion
```javascript
// JavaScript version of: (unsigned)
//  printf "%0*d" width num
function leftFillNum(num, targetLength) {
  return num.toString().padStart(targetLength, 0);
}

const num = 123;
console.log(leftFillNum(num, 5));
// expected output: "00123"
```
