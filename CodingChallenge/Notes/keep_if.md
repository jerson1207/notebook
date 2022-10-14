# keep_if()
Deletes every element of self for which the given block evaluates to false.
_If no block is given, an **Enumerator** is returned instead._

```ruby
a = %w{ a b c d e f }
a.keep_if { |v| v =~ /[aeiou]/ }  #=> ["a", "e"]
```
#### Hide source
```
static VALUE
rb_ary_keep_if(VALUE ary)
{
    RETURN_SIZED_ENUMERATOR(ary, 0, 0, ary_enum_length);
    rb_ary_select_bang(ary);
    return ary;
}
```
