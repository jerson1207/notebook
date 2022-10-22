# Check for Anagrams
Create a function that takes two strings and returns either true or false depending on whether they're anagrams or not.

### Examples
```
isAnagram("cristian", "Cristina") ➞ true

isAnagram("Dave Barry", "Ray Adverb") ➞ true

isAnagram("Nope", "Note") ➞ false
```

#### Solutions
```javascript
function isAnagram(s1, s2) {
  var str1 = s1.toLowerCase().split('').sort().join('').trim();
  var str2 = s2.toLowerCase().split('').sort().join('').trim();
  return str1===str2;
}
```

```javascript
function isAnagram(s1, s2) {
  var t = s => s.toLowerCase().split('').sort().join('');
  return t(s1) === t(s2); 
}
```

```javascript
function isAnagram(s1, s2) {
  return JSON.stringify(s1.toLowerCase().split('').sort()) == JSON.stringify(s2.toLowerCase().split('').sort());
}
```
