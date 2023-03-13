---
title: What is the ruby equivalent to python's "s= "hello, %s. where is %s?" % ("john","mary")"?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: The equivalent Ruby code would be `s = `hello, %s. Where is %s?` % [`John`, `Mary`]`.
---

**Contents**

[TOC]

## String Interpolation in Ruby

In Ruby, string interpolation is done using the `#{}` syntax. We can directly include variables, expressions within a string using this syntax. 

```ruby
name = "John"
place = "Mary"

s = "hello, #{name}. Where is #{place}?"
puts s
```

Output:
```
hello, John. Where is Mary?
```

## String Formatting in Ruby

Ruby also has a String#% method that can be used for string formatting. We can specify the format of our output using this method. 

```ruby
s = "hello, %s. Where is %s?" % ["John", "Mary"]
puts s
```

Output:
```
hello, John. Where is Mary?
```

We use `%s` to specify a string data type in the format string. We can pass an array of values to the `%` operator. 

## Using Named Placeholders in Ruby

We can use named placeholders using the `%{}` syntax in Ruby. We can use the named placeholders to format and insert values within a string.

```ruby
s = "hello, %{name}. Where is %{place}?" % {name: "John", place: "Mary"}

puts s
```

Output:
```
hello, John. Where is Mary?
```

We use `%{}` to specify a named placeholder. We create a hash with key-value pairs where the key is the name of the placeholder and the value is the value to be inserted. 

## Conclusion

In Ruby, we can use string interpolation using the `#{}` syntax or use the `%` operator with placeholders. We can use `%s` to specify a string data type in the format string or use named placeholders using the `%{}` syntax.
