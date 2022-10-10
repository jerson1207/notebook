# Basic E-Mail Validation
Create a function that accepts a string, checks if it's a valid email address and returns either true or false, depending on the evaluation.
- The string must contain an @ character.
- The string must contain a . character.
- The @ must have at least one character in front of it.
  - e.g. "e@edabit.com" is valid while "@edabit.com" is invalid.
- The . and the @ must be in the appropriate places.
  - e.g. "hello.email@com" is invalid while "john.smith@email.com" is valid.

If the string passes these tests, it's considered a valid email address.
### Example
```
validate_email("@gmail.com") ➞ false

validate_email("hello.gmail@com") ➞ false

validate_email("gmail") ➞ false

validate_email("hello@gmail") ➞ false

validate_email("hello@edabit.com") ➞ true
```
### Notes
- Check the Tests tab to see exactly what's being evaluated.
- You can solve this challenge with RegEx, but it's intended to be solved with logic.
- Solutions using RegEx will be accepted but frowned upon :(

---
```ruby
def validate_email(str)
	str.include?('@') && str.include?('.') && !str.index('@').zero? && str.index('@') < str.rindex('.')
end
```
```ruby
def validate_email(str)
	!!str.match(/[a-z]+@[a-z]*\.[a-z]*/i)
end
```
```ruby
def validate_email(str)
  i = str.index('@', 1)
  !!(i && str.index('.', i))
end
```
