# Array
>> **_Index start at 0_**

#### .first
- The .first method accesses the first element of the array, the element at index 0:
```ruby
  arr = [0, 1, 2, 3, 4]
  arr.first
  // 0
```
#### .last
- The .last method accesses the last element of the array:
```ruby
  arr = [0, 1, 2, 3, 4]
  arr.last
  // 4
```

#### .take
- The .take method returns the first n elements of the array:

```ruby
  arr = [0, 1, 2, 3, 4]
  
  arr.take
  //in `take': wrong number of arguments (given 0, expected 1) (ArgumentError)
  
  arr.take(0)
  // []

  arr.take(1)
  // [0]
  
  arr.take(3)
  //[0, 1, 2]
  
  arr.take(-1)
  //in `take': attempt to take negative size (ArgumentError)
```

#### .drop
- The .drop method returns the elements after n elements of the array:

```ruby
  arr = [0, 1, 2, 3, 4]
  
  arr.drop
  // in `drop': wrong number of arguments (given 0, expected 1) (ArgumentError)
  
  arr.drop(0)
  // [0, 1, 2, 3, 4]
  
  arr.drop(1)
  // [1, 2, 3, 4]
  
    arr.drop(3)
  // [3, 4]
  
  arr.drop(-1)
  // in `drop': attempt to drop negative size (ArgumentError)
```

### array index
- You can access a specific element in an array by accessing its index. If the index does not exist in the array, nil will be returned:
```ruby
  arr = [0, 1, 2, 3, 4]
  
  arr[0]
  // 0
  
  arr[3]
  // 3
  
  arr[0..3]
  //[0, 1, 2, 3]
  // return range from start selected index to the last index
  
  arr[0...3]
  [0, 1, 2]
  // return range from start selected index to the last index and omit the last element
  // return first to the last
  
  arr[-1]
  // 4
  // return 2nd to the last
  
  arr[-2]
  //3


