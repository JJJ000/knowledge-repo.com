---
title: Rephrased regular expressions in Python that are not greedy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Non-greedy regexes in Python match the shortest possible substring that satisfies the pattern.
---

**Contents**

[TOC]

Introduction to Non-Greedy Regexes in Python

Regexes or regular expressions are patterns used to search and manipulate text. Python has a built-in module called `re` that provides support for regular expressions. One of the concepts in regular expressions is *greediness*, which refers to how much text a pattern should try to match. By default, regular expressions in Python are greedy, which means that they try to match as much text as possible. This behavior may not always be desirable, especially in cases where there are multiple matches in a string, and we want to retrieve the smallest match possible. In such cases, non-greedy or lazy matching can be used.

What are non-greedy regexes?

Non-greedy or lazy matching refers to a type of regular expression matching in which the pattern matches the smallest possible set of characters rather than the maximum possible. This behavior is denoted by adding a question mark "?" to the end of a quantifier in a regular expression. Quantifiers are the characters that specify how many times a pattern should match, such as "*" for zero or more matches, "+" for one or more matches, and "?" for zero or one match. The question mark "?" after a quantifier changes the quantifier from greedy to non-greedy. 

For example, consider the regular expression `a.*b` and the string `aabb`. The dot (".") in the regex matches any character, and the asterisk ("*") quantifier after it means that it should match zero or more occurrences of the preceding character. The resulting regex tries to match as many characters as possible between "a" and "b". When applied to the string `aabb`, the regex matches the entire string "aabb". However, if we make the regex non-greedy by adding a question mark after the asterisk like so: `a.*?b`, the regex only matches the substring "aab". 

Example Use of Non-Greedy Regexes in Python

Consider the following Python code snippet that applies a greedy regex pattern to a string containing multiple occurrences of a pattern:

```
import re
  
text = "apple banana cherry grapefruit"
pattern = "a.*t"
result = re.findall(pattern, text)
print(result)
```

The regex pattern `a.*t` matches any substring that starts with "a" and ends with "t" and can contain any number of characters in between. When applied to the `text` string, the `findall()` function returns a list of all the substrings that match this pattern. The resulting list includes two matches: `['apple banana cherry']` and `['grapefrui']`. However, since the pattern is greedy, the first match includes more characters than we want (i.e., "cherry" is included). 

To make the matching non-greedy, we can modify the pattern by adding a question mark after the asterisk, as shown below:

```
import re
  
text = "apple banana cherry grapefruit"
pattern = "a.*?t"
result = re.findall(pattern, text)
print(result)
```

Now, the `findall()` function returns a list of the substrings that match the non-greedy pattern, resulting in `['apple', 'banan', 'grapefrui']`. The match for the first occurrence of "a.*t" now only includes the smallest possible substring, starting from "a" and ending at "t".

Conclusion

In summary, non-greedy or lazy matching refers to a regular expression matching pattern that matches the smallest possible set of characters instead of the maximum possible set. We can make a regular expression pattern non-greedy by appending a question mark to a quantifier in the pattern. Non-greedy matching can be useful when there are multiple matches in a string, and we want to retrieve the smallest possible match for each.
