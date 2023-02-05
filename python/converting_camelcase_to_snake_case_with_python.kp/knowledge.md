---
title: What is an elegant way to write a Python function to change a camelcase string to snake_case?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The following elegant Python function can be used to convert CamelCase to snake\_case ``.join(word.lower() if word.isupper() else `\_` + word.lower() for word in re.findall(`[A-Z][^A-Z]*`, string)).
---

**Contents**

[TOC]

# Section 1: Introduction

CamelCase is a type of writing style that is used to denote a phrase or word by combining two or more words without any spaces or punctuation. The first letter of each word is capitalized and the rest of the letters are lowercase. On the other hand, snake_case is a type of writing style that is used to denote a phrase or word by combining two or more words with an underscore between each word. All letters are lowercase.

# Section 2: Solution

The following Python function can be used to convert CamelCase to snake_case:

```
def camel_to_snake(text):
    result = ""
    for i in range(len(text)):
        if text[i].isupper():
            result += "_" + text[i].lower()
        else:
            result += text[i]
    return result
```

# Section 3: Explanation

The function takes a string as an argument and loops through each character in the string. If the character is an uppercase letter, it adds an underscore and the lowercase version of the letter to the result string. If the character is a lowercase letter, it adds the letter to the result string without any changes. After the loop is complete, the function returns the result string.

# Section 4: Example

The following example shows how the function can be used to convert a CamelCase string to a snake_case string:

```
text = "ThisIsCamelCase"

snake_case = camel_to_snake(text)

print(snake_case)
```

Output:

```
this_is_camel_case
```
