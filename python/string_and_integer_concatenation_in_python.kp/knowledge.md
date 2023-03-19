---
title: Combining text and numerical values in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You can concatenate a string and an integer in Python by converting the integer to a string using the str() function and then using the concatenation operator (+).
---

**Contents**

[TOC]

Section 1: Converting integer to string

Before concatenating an integer and string in Python, we need to make sure that the integer value is converted to a string. We can do that using the built-in str() function in Python. The str() function takes an integer argument and returns its string representation. Here's an example:

```
number = 10
number_str = str(number)
```

In this example, we are converting the integer value 10 to its string representation using the str() function and storing it in the variable number_str.

Section 2: Concatenating string and integer

Once we have an integer in its string representation, we can concatenate it with other string values using the + operator. Here's an example:

```
name = "John"
age = 30
message = "My name is " + name + " and I am " + str(age) + " years old."
print(message)
```

Output:
```
My name is John and I am 30 years old.
```

In this example, we are concatenating the string "My name is " with the value of the variable name, followed by the string " and I am ", followed by the value of the variable age in its string representation, and finally, the string " years old." We are using str(age) to convert the integer value of age to its string representation before concatenating it with the other string values.

Section 3: F-strings

Another way to concatenate strings and variables in Python is by using f-strings. An f-string is a formatted string literal that allows us to embed expressions inside string literals. Here's an example:

```
name = "John"
age = 30
message = f"My name is {name} and I am {age} years old."
print(message)
```

Output:
```
My name is John and I am 30 years old.
```

In this example, we are using f-strings to embed the values of the variables name and age inside the string literal. The expressions are enclosed in curly braces {} and prefixed with the letter f to indicate that it is an f-string.

Section 4: Conclusion

In Python, we can concatenate strings and integer values by converting the integer to its string representation using the str() function and then concatenating it with other string values using the + operator or f-strings. The choice between using + and f-strings depends on personal preference and the complexity of the expression being embedded in the string literal.
