# Find the Missing Number
Create a function that takes an array of numbers between 1 and 10 (excluding one number) and returns the missing number.
### Examples
```
missingNum([1, 2, 3, 4, 6, 7, 8, 9, 10]) ➞ 5

missingNum([7, 2, 3, 6, 5, 9, 1, 4, 8]) ➞ 10

missingNum([10, 5, 1, 2, 4, 6, 8, 3, 9]) ➞ 7
```
### Notes
- The array of numbers will be unsorted (not in order).
- Only one number will be missing.
___
```javascript
function missingNum(arr) {
  var sum = arr.reduce((a, b) => a + b, 0);
  return 55 - sum;
}
```
```javascript
function missingNum(arr) {
  return 55-arr.reduce((acc,x) => acc+x);
}
```
```javascript
function missingNum(arr) {
  for(var i = 1; i <= 10; i++){
    if(arr.indexOf(i) == -1) return i
  }
}
```
```javascript
function missingNum(arr) {
  return 55 - arr.reduceRight(function(a,b){return a+b;})
}
```
