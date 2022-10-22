# Reverse Words in a String
Given an input string, reverse the string word by word, the first word will be the last, and so on.
### Examples
~~~
reverseWords(" the sky is blue") ➞ "blue is sky the"

reverseWords("hello   world!  ") ➞ "world! hello"

reverseWords("a good example") ➞ "example good a"
~~~
___
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
```javascript
function removeDups(arr) {
  var newArr = [];
  for (i of arr) {
    if (newArr.indexOf(i) == -1) {
      newArr.push(i)
    }
  }
  return newArr;
}
```
