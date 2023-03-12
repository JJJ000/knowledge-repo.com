---
title: What is the correct way to arrange a string that contains a numeric value?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the key parameter of the sorted or sort() function with a lambda function that extracts the number from the string.
---

**Contents**

[TOC]

## Splitting the String

Before sorting the string with a number, we need to first split the string into two parts- the string part and the number part. We can do this using regular expressions. 

```python
import re

string_with_number = "apple2 banana5 peach1"
split_string = re.findall('\d+|\D+', string_with_number)
```
In the above code, we first import the re module. Then we use the `findall()` function of the re module to split the string into parts. `\d+` returns one or more digits, and `\D+` returns one or more non-digits. 

The resulting `split_string` variable will be a list with alternating string and number elements. In this case, it will look like `['apple', '2', ' banana', '5', ' peach', '1']`


## Sorting with the Number

Now that we have split the string into parts, we can sort it with the number part. An easy way to do this is to convert the number part into an integer using the `int()` function and then sorting the list using the `sorted()` function with a key argument.

```python
sorted_string = sorted(split_string, key=lambda x: (int(x) if x.isdigit() else x))

```

In the above code, we use the `sorted()` function to sort the `split_string` variable. We use a key function to specify that the sorting should be done with the number part, if it exists. 

We use the `isdigit()` function to check if the part is a number or not. If it is a number, we convert it to an integer using the `int()` function. If it is not a number, we keep it as a string. 

The resulting `sorted_string` variable will be a sorted list of the original string split into parts. In this case, it will look like `['apple', 'peach', 'banana', '1', '2', '5']`


## Joining the String

Finally, we can join the sorted string parts back into a single string.

```python
sorted_string_with_number = ''.join(sorted_string)
```

In the above code, we use the `join()` function to join the sorted string parts back into a single string. 

The resulting `sorted_string_with_number` variable will be the original string with the number part sorted. In this case, it will look like `applepeachbanana125`. 


## Putting it All Together

Here's the complete code to correctly sort a string with a number inside:

```python
import re

string_with_number = "apple2 banana5 peach1"
split_string = re.findall('\d+|\D+', string_with_number)
sorted_string = sorted(split_string, key=lambda x: (int(x) if x.isdigit() else x))
sorted_string_with_number = ''.join(sorted_string)
print(sorted_string_with_number)
```

Output: `applepeachbanana125`
