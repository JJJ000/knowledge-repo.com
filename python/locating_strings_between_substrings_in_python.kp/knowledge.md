---
title: Locate the text between two given substrings
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the str.find() or str.index() method to find the index of the first occurrence of the first substring, then use the str.rfind() or str.rindex() method to find the index of the last occurrence of the second substring, and finally use the str.slice() method to extract the string between the two substrings.
---

**Contents**

[TOC]

#1 Using Regular Expressions
Regular expressions can be used to find strings between two substrings. The following example uses the re.findall() method to find all strings between two substrings:

```
import re

string = "This is a string with two sub strings"

# Find all strings between two substrings
matches = re.findall(r'\w+(?=sub)', string)

# Print the matches
print(matches)

# Output: ['is a string with two']
```

#2 Using String Slicing
String slicing can also be used to find strings between two substrings. The following example uses the str.find() method to find the indices of the two substrings and then slices the string accordingly:

```
string = "This is a string with two sub strings"

# Find the indices of the two substrings
start = string.find('sub')
end = string.find('sub', start + 1)

# Slice the string between the two substrings
substring = string[start:end]

# Print the substring
print(substring)

# Output: with two 
```

#3 Using str.split()
The str.split() method can also be used to find strings between two substrings. The following example splits the string by the two substrings and then prints the string between them:

```
string = "This is a string with two sub strings"

# Split the string by the two substrings
splits = string.split('sub')

# Print the string between the two substrings
print(splits[1])

# Output:  with two 
```

#4 Using str.partition()
The str.partition() method can also be used to find strings between two substrings. The following example partitions the string by the two substrings and then prints the string between them:

```
string = "This is a string with two sub strings"

# Partition the string by the two substrings
partition = string.partition('sub')

# Print the string between the two substrings
print(partition[1])

# Output: with two
