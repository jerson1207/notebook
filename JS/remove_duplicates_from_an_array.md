# Remove Duplicates from an Array
Create a function that takes an array of items, removes all duplicate items and returns a new array in the same sequential order as the old array (minus duplicates).
### Examples
~~~
removeDups([1, 0, 1, 0]) ➞ [1, 0]

removeDups(["The", "big", "cat"]) ➞ ["The", "big", "cat"]

removeDups(["John", "Taylor", "John"]) ➞ ["John", "Taylor"]
~~~
### Notes
- Tests contain arrays with both strings and numbers.
- Tests are case sensitive.
- Each array item is unique.
___

```javascript
function removeDups(arr) {
  return [...new Set(arr)];
}
```
```javascript
function removeDups(arr) {
  return arr.filter((x, i, a) => a.indexOf(x) === i);
}
```
```javascript
function removeDups(arr) {
  var returnArr = [];
  for(var i = 0; i < arr.length; i++) {
    if(returnArr.indexOf(arr[i]) === -1) {
      returnArr.push(arr[i]);
    }
  }
  return returnArr;
}
```
```javascript
function removeDups(arr) {
  var used = [];
  arr.forEach(function(item){
    if (!used.includes(item)){
      used.push(item);
    }
  });
  return used;
}
```
