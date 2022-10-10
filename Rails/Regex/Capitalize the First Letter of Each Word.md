# Capitalize the First Letter of Each Word
Create a function that takes a string as an argument and converts the first character of each word to uppercase. Return the newly formatted string.

### Examples
```
make_title("This is a title") ➞ "This Is A Title"

make_title("capitalize every word") ➞ "Capitalize Every Word"

make_title("I Like Pizza") ➞ "I Like Pizza"

make_title("PIZZA PIZZA PIZZA") ➞ "PIZZA PIZZA PIZZA"
```
### Notes
- You can expect a valid string for each test case.
- Some words may contain more than one uppercase letter (see example #4).

### Resources
- [map array](https://apidock.com/ruby/Array/map)
- [split array](https://apidock.com/ruby/String/split)
- [join array](https://apidock.com/ruby/Array/join)
---
```ruby
def make_title(s)
  s.gsub(/(^|\s)./, &:upcase)
end
```
```ruby
def make_title(str)
  str.split(' ').map! { |word| word[0].upcase + word[1..-1] }.join(' ')
end
```
```ruby
def make_title(str)
  str.split.each {|word| word[0] = word[0].upcase}.join(" ")
end
```
