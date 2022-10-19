# JavaScript String **trim()**

### Definition and Usage
- The _trim()_ method removes whitespace from both sides of a string.
- The _trim()_ method does not change the original string.

### Syntax
```
string.trim()
```

### Example 1
```javascript
let text = "       Hello World!        ";
let result = text.trim();
```
> **Note**
> result value is now equal to "Hello World!"

## JavaScript String **trimEnd()**
### Definition and Usage
- The trimEnd() method removes whitespace from the end of a string.
- The trimEnd() method does not change the original string.
- The trimEnd() method works like trim(), but removes whitespace only from the end of a string.
### Syntax
```javascript
string.trimEnd()
```
### Example
```javascript
<h1>JavaScript Strings</h1>
<h2>The trimEnd() Method</h2>

<p id="demo"></p>

<script>
let text1 = "     Hello World!     ";
let text2 = text1.trimEnd();

document.getElementById("demo").innerHTML =
"Length text1 = " + text1.length + "<br>Length text2 = " + text2.length;
</script>
```
```html
JavaScript Strings
The trimEnd() Method
Length text1 = 22
Length text2 = 17
```
