# Array

#### .pop
- The .pop method **will permantently remove the last element of an array**:

```ruby
def array_methods
  arr = [0, 1, 2, 3, 4]
  p arr.pop
  p arr
end

array_methods
# 4
# [0, 1, 2, 3]
```

#### .shift
- The .shift method **will permantently remove the first element of an array and return this** element:

```ruby
def array_methods
  arr = [0, 1, 2, 3, 4]
  p arr.shift
  p arr
end

array_methods
# 0
# [1, 2, 3, 4]
```

#### .push
- The .push method **will allow you to add an element to the end of an array:**
```ruby
  arr = [0, 1, 2, 3, 4]
  arr.push(99)
  # 0, 1, 2, 3, 4, 99]
```

####.unshift
- The .unshift method will allow you to add an element to the beginning of an array:

```ruby
  arr = [0, 1, 2, 3, 4]
  arr.unshift(99)
  # [99, 0, 1, 2, 3, 4]
```

#### .delete
- The .delete method removes a specified element from an array permanently

```ruby
def array_methods
  arr = [0, 1, 2, 3, 4]
  arr.delete(3)
  arr
end

p array_methods
# [0, 1, 2, 4]
```

#### .delete_at
- The .delete_at method allows you to permanently remove an element of an array at a specified index
```ruby
def array_methods
  arr = [0, 1, 2, 3, 4, 99]
  arr.delete_at(5)

  arr
end
p array_methods
# [0, 1, 2, 3, 4]
```








