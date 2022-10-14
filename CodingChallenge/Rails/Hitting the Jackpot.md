# Hitting the Jackpot
Create a function that takes an array (slot machine outcome) and returns true if all elements in the array are identical, and false otherwise. The array will contain 4 elements.
### Examples
```
test_jackpot(["@", "@", "@", "@"]) ➞ true

test_jackpot(["abc", "abc", "abc", "abc"]) ➞ true

test_jackpot(["SS", "SS", "SS", "SS"]) ➞ true

test_jackpot(["&&", "&", "&&&", "&&&&"]) ➞ false

test_jackpot(["SS", "SS", "SS", "Ss"]) ➞ false
```
### Notes
The elements must be exactly identical for there to be a jackpot.
### Codes
```ruby
def test_jackpot(result)
  result.uniq.count == 1
end
```

```ruby
def test_jackpot(result)
  result.select { |e| e != r[0] }.empty?
end
```

```ruby
def test_jackpot(result)
  result[1] == result[0] && result[2] == result[0] && result[3] == result[0]
end
```
