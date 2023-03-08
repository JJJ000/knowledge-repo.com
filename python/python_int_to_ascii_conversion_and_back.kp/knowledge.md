---
title: In python, how to change an integer to ascii and then back again?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: In order to convert an integer to its corresponding ASCII character and then back to the integer again in Python, use the built-in functions chr() and ord(), respectively.
---

**Contents**

[TOC]

Converting Int to ASCII in Python

To convert an integer to ASCII in Python, we can use the chr() function. The chr() function takes an integer as an argument and returns the corresponding ASCII character.

``` python
# Example code to convert int to ascii
num = 65
ascii_value = chr(num)
print(ascii_value) # Output: A
```

In this example, we pass the integer 65 to the chr() function, which corresponds to the ASCII value of the uppercase letter 'A'. The output of the code snippet will be the character 'A'.

Converting ASCII to Int in Python

To convert an ASCII character back to its corresponding integer value in Python, we can use the ord() function. The ord() function takes an ASCII character as an argument and returns its corresponding integer value.

``` python
# Example code to convert ascii to int
char = 'A'
int_value = ord(char)
print(int_value) # Output: 65
```

In this example, we pass the character 'A' to the ord() function, which returns the integer value 65 This corresponds to the ASCII value of the uppercase letter 'A'. The output of the code snippet will be the integer 65.

Handling Errors

It is important to note that both the chr() and ord() functions can raise a ValueError exception if we pass an invalid input. For example, passing a value that is not an integer to chr() can raise an exception.

``` python
# Example code to show ValueError 
num = 'a'
ascii_value = chr(num)  # This will throw ValueError

char = '&'
int_value = ord(char) # This will throw ValueError
```

In these examples, we pass invalid values 'a' and '&' to the chr() and ord() functions, respectively. Both of these will throw ValueError exceptions because these values are not valid integers or ASCII characters.

Conclusion

In Python, we can use the chr() function to convert an integer to its corresponding ASCII character, and the ord() function to convert an ASCII character to its corresponding integer value. We should ensure to handle any input errors and validate that the input values are correct before attempting to convert them.
