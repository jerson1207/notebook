# Finding Common Elements
Create a function that takes two lists of numbers sorted in ascending order and returns an array of numbers which are common to both the input arrays.
### Examples
```
common_elements([-1, 3, 4, 6, 7, 9], [1, 3]) ➞ [3]

common_elements([1, 3, 4, 6, 7, 9], [1, 2, 3, 4, 7, 10]) ➞ [1, 3, 4, 7]

common_elements([1, 2, 2, 2, 3, 4, 5], [1, 2, 4, 5]) ➞ [1, 2, 4, 5]

common_elements([1, 2, 3, 4, 5], [10, 12, 13, 15]) ➞ []
```
### Note
- Lists are sorted.
- Try doing this problem with O(n + m) time complexity.

---
```ruby
def common_elements(arr1, arr2)
  arr1 & arr2
end
```
```ruby
def common_elements(arr1, arr2)
  arr1.uniq.select { |n| arr2.include?(n) }
end
```
```ruby
def common_elements(arr1, arr2)
  a = arr1.uniq+arr2.uniq
  a.keep_if{|x| a.count(x) > 1 }.uniq
end
```
```ruby
def common_elements(arr1, arr2)
	arr1.inject([]){|memo, el| arr2.include?(el) ? memo << el : memo}.uniq
end
```
