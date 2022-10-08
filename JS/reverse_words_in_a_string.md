# How Much is True?
Create a function which returns the number of true values there are in an array.
### Examples
~~~
reverseWords(" the sky is blue") ➞ "blue is sky the"

reverseWords("hello   world!  ") ➞ "world! hello"

reverseWords("a good example") ➞ "example good a"
~~~
## Code
```javascript
function reverseWords(s) {
	return s.trim().replace(/ +/,' ').split(' ').reverse().join` `
}
```
```javascript
function reverseWords(s) {
	return s.split(" ").reverse().join(" ")
}
```
```javascript
function reverseWords(string) {
	return string.trim().split(/\s+/).reverse().join(' ')
}
```
