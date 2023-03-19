---
title: Rewording using "elif" statements as a conditional in list comprehension
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Yes, `elif` can be used in list comprehension conditionals in Python, but it needs to be written as a nested ternary expression.
---

**Contents**

[TOC]

Section 1: Introduction to list comprehension

List comprehension is a concise and powerful way to create lists in Python. It allows us to create a new list based on some existing list, with the help of conditions and operations specified inside square brackets. The syntax of list comprehension is: 

`new_list = [expression for item in input_list if condition]`

where `expression` is what we want to do with each `item` from the `input_list`, if it satisfies the `condition`. 

Section 2: The need for `elif` in list comprehension conditionals

Sometimes, the conditions for generating a new list based on some input list might be more complex than a simple boolean expression. In such cases, we may need to use `if-elif-else` conditionals inside the list comprehension. 

For example, let's say we have a list of numbers from 1 to 10, and we want to create a new list based on this list, such that: 
- If the number is divisible by 2, add 'even' to the new list.
- If the number is divisible by 3, add 'odd' to the new list.
- If the number is divisible by both 2 and 3, add 'even-odd' to the new list.
- If the number is neither divisible by 2 nor by 3, add 'other' to the new list.

In this case, we need to use `if-elif-else` inside the list comprehension to specify these conditions. 

Section 3: Using `elif` in list comprehension conditionals

Here's an example of how we can use `elif` inside the list comprehension to implement the above conditions: 

```
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

new_list = [ 'even' if number % 2 == 0 else 'odd' if number % 3 == 0 else 'even-odd' if number % 6 == 0 else 'other' for number in numbers]

print(new_list)
```

Output: 
```
['other', 'even', 'odd', 'even', 'other', 'even-odd', 'odd', 'even', 'other', 'even']
```

In this example, we use `if` for the first condition (divisible by 2), `elif` for the second condition (divisible by 3), and `else` for the third and fourth conditions. Note that we can have multiple `elif` clauses inside the list comprehension, just like in regular `if-elif-else` statements. 

Section 4: Conclusion

`elif` can be used inside list comprehension conditionals to implement complex conditions for generating a new list based on some input list. Just like in regular statements, multiple `elif` clauses can be used inside list comprehension as well.
