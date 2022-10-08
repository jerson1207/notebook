# YouTube Upload Count
You are given an array of dates in the format Dec 11 and a month in the format Dec as arguments. Each date represents a video that was uploaded on that day. Return the number of uploads for a given month.
### Examples
~~~
upload_count(["Sept 22", "Sept 21", "Oct 15"], "Sept") ➞ 2

upload_count(["Sept 22", "Sept 21", "Oct 15"], "Oct") ➞ 1
~~~
### Note
If you only pay attention to the month and ignore the day, the challenge will become easier.

---
```ruby
def upload_count(dates, month)
  dates.count { |d| d.start_with?(month) }
end
```
```ruby
def upload_count(dates, month)
  dates.select{|a| a.include? month}.count	
end
```
```ruby
def upload_count(d, m)
  d.grep(/#{m}/).count
end
```
