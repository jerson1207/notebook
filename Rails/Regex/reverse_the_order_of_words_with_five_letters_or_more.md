# Reverse the Order of Words with Five Letters or More
Write a function that takes a string of one or more words as an argument and returns the same string, but with all five or more letter words reversed. Strings passed in will consist of only letters and spaces. Spaces will be included only when more than one word is present.
### Examples
```
everse("Reverse") ➞ "esreveR"

reverse("This is a typical sentence.") ➞ "This is a lacipyt .ecnetnes"

reverse("The dog is big.") ➞ "The dog is big."
```
### Notes
You can expect a valid string to be provided for each test case.

---
```ruby
def reverse(str)
  str.split(' ').map { |item| item.size >= 5 ? item.reverse() : item }.join(' ')
end
```
```ruby
def reverse(str)
	words = str.split(" ")
	words.each_with_index { |word, index|
		if word.length() >= 5
			words[index] = word.reverse
		end
	}
	words.join(" ")
end
```
```ruby
def reverse(str)
	new = []
	str.split(" ").map do |part|
		if part.length >= 5
			new << part.reverse
		else new << part
		end
	end
	return new.join(" ")
end
```



