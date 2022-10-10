# No Yelling
Create a function that transforms sentences ending with multiple question marks ? or exclamation marks ! into a sentence only ending with one without changing punctuation in the middle of the sentences.
### Examples
```
no_yelling("What went wrong?????????") ➞ "What went wrong?"

no_yelling("Oh my goodness!!!") ➞ "Oh my goodness!"

no_yelling("I just!!! can!!! not!!! believe!!! it!!!") ➞ "I just!!! can!!! not!!! believe!!! it!"
# Only change repeating punctuation at the end of the sentence.

no_yelling("Oh my goodness!") ➞ "Oh my goodness!"
# Do not change sentences where there exists only one or zero exclamation marks/question marks.

no_yelling("I just cannot believe it.") ➞ "I just cannot believe it."
```
### Notes 
- Only change ending punctuation - keep the exclamation marks or question marks in the middle of the sentence the same (see third example).
- Don't worry about mixed punctuation (no cases that end in something like ?!??!).
- Keep sentences that do not have question/exclamation marks the same.

### Resources
- [Ruby Strings Cheat Sheet](https://www.shortcutfoo.com/app/dojos/ruby-strings/cheatsheet)
- [RegExr: Learn, Build, & Test RegEx](https://www.shortcutfoo.com/app/dojos/ruby-strings/cheatsheet)
- [Class: Regexp](https://ruby-doc.org/core-2.2.0/Regexp.html)
---
```ruby
def no_yelling(phrase)
	phrase.gsub(/\?+$/, '?').gsub(/!+$/, '!')
end
```
```ruby
def no_yelling(phrase)
	phrase.sub(/\!+\z|\?+\z/) { |m| m.include?('!') ? '!' : '?' }
end
```
```ruby
def no_yelling(phrase)
  last_char = phrase[-1]
  return phrase.gsub(phrase.split(" ")[-1], phrase.split(" ")[-1].squeeze(last_char))
end
```
