---
title: In python, concatenate a series of strings and enclose each one within double quotes
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use a list comprehension with f-strings to join the list of strings while wrapping each string in quotation marks.
---

**Contents**

[TOC]

## Step 1: Create a List of Strings

The first step is to create a list of strings that we want to join and wrap in quotation marks. For this example, we'll create a list of three strings:

```python
strings = ['apple', 'banana', 'orange']
```

## Step 2: Use Join Function to Join Strings

Next, we'll use the `join()` function to join the strings in our list:

```python
joined_strings = ', '.join(strings)
```

This will join our list of strings with commas and spaces between each string, resulting in a single string:

```
'apple, banana, orange'
```

## Step 3: Wrap Strings in Quotation Marks

Now that we have a single string with our original strings joined together, we can wrap each string in quotation marks. We can do this using a list comprehension:

```python
quoted_strings = ['"' + s + '"' for s in strings]
```

This will create a new list where each string is wrapped in quotation marks:

```
['"apple"', '"banana"', '"orange"']
```

## Step 4: Join Quoted Strings

Finally, we can join our quoted strings using the `join()` function:

```python
quoted_joined_strings = ', '.join(quoted_strings)
```

This will result in a single string where each string is wrapped in quotation marks and joined with commas and spaces between each string:

```
'"apple", "banana", "orange"'
```

Putting it all together, here's the complete code:

```python
strings = ['apple', 'banana', 'orange']
joined_strings = ', '.join(strings)
quoted_strings = ['"' + s + '"' for s in strings]
quoted_joined_strings = ', '.join(quoted_strings)
print(quoted_joined_strings)
```
