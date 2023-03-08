---
title: What is the technique for substituting the final instance of a pattern within a string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: You can use rfind() method to locate the last occurrence of the expression in the string and then use replace() method to replace it.
---

**Contents**

[TOC]

Section 1: Introduction

Python is a widely used programming language for a variety of applications, including data analysis and machine learning. It also offers many built-in functions that facilitate various operations, including string manipulation. This article focuses on how to replace the last occurrence of an expression in a string in Python.

Section 2: Overview of the problem

Python provides the replace() function to replace a string's all occurrences with another string. However, it does not offer a built-in function to replace the last occurrence of a string in a string. Therefore, we need to use other techniques to find the last occurrence and replace the string. 

Section 3: Solution to the problem

One of the simple ways to replace the last occurrence of a string in a string is to use the rfind() method to find the last occurrence of the string and then use string slicing and concatenation to replace the string with the desired value.

```python
text = "Replace the last occurrence of Replace"
last_occurrence = text.rfind("Replace")
new_text = text[:last_occurrence] + "Inject" + text[last_occurrence+len("Replace"):]
print(new_text)
```

Output: `Replace the last occurrence of Inject`

In the above example, we find the last occurrence of the string "Replace" using rfind() method and store it in the last_occurrence variable. Then we use string slicing and concatenation to replace the last occurrence of the string with "Inject." 

Section 4: Conclusion

In conclusion, Python does not offer a built-in function to replace the last occurrence of a string in a string. However, we can use the rfind() method to find the last occurrence and then use string slicing and concatenation to replace the string with the desired value. This method is simple and provides an effective solution to the problem.
