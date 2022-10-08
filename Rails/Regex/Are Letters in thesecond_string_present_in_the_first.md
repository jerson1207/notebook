# Are Letters in the Second String Present in the First?
Create a function that accepts an array of two strings and checks if all of the letters in the second string are present in the first string.
### Examples

```
letter_check(["trances", "nectar"]) ➞ true

letter_check(["compadres", "DRAPES"]) ➞ true

letter_check(["parses", "parsecs"]) ➞ false
```
### Notes
- Function should not be case sensitive (as indicated in the second example).
- Both strings are presented as a single argument in the form of an array.
- Bonus: Solve this without RegEx.

---

```ruby
def letter_check(arr)
  arr[1].downcase.delete(arr[0].downcase) == ''
end
```
```ruby
def letter_check(arr)
  parent_str, child_str = arr
  parent_chars = Set.new(parent_str.chars.map(&:downcase))
  child_str.downcase.each_char do | char | 
    return false unless parent_chars.include?(char)
  end
  true
end
```
```ruby
def letter_check(arr)
  arr.last.chars.all? { |ch| arr[0].downcase.include?(ch.downcase) }
end
```
