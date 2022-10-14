# Return Only the Integer
Write a function that takes an array of elements and returns only the integers.

### Examples
```
return_only_integer([9, 2, "space", "car", "lion", 16]) ➞ [9, 2, 16]

return_only_integer(["hello", 81, "basketball", 123, "fox"]) ➞ [81, 123]

return_only_integer([10, "121", 56, 20, "car", 3, "lion"]) ➞ [10, 56, 20, 3]

return_only_integer(["String",  true,  3.3,  1]) ➞ [1]
```
### Code
```ruby
def return_only_integer(arr)
  arr.grep Integer
end
```

```ruby
def return_only_integer(arr)
  arr.select{ |v| v.is_a? Integer }
end
```

```ruby
def return_only_integer(arr)
  return arr.select {|i| i.class == Fixnum}
end
```

```ruby
def return_only_integer(a)
  a.keep_if { |e| e.is_a?(Integer) }
end
```
