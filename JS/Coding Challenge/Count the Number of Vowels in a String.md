# Count the Number of Vowels in a String




Count the Number of Vowels Using Regex
```javascript
function countVowel(str) { 
  // find the count of vowels
  const count = str.match(/[aeiou]/gi).length;
  
  // return number of vowels
  return count;
}
```

Count the Number of Vowels Using for Loop
```javascript
// defining vowels
const vowels = ["a", "e", "i", "o", "u"]

function countVowel(str) {
  // initialize count
  let count = 0;
  
  // loop through string to test if each character is a vowel
  for (let letter of str.toLowerCase()) {
    if (vowels.includes(letter)) {
      count++;
    }
  }

  // return number of vowels
  return count
}
```
