---
title: What is the process for determining the number of times a string appears in another string?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the String.prototype.match() method to count the occurrence of a string in another string.
---

**Contents**

[TOC]

# Section 1: Using for loop

1. Initialize a counter variable to 0.
2. Use a for loop to iterate through the string.
3. Inside the loop, use an if statement to check if the current character is equal to the string you want to count.
4. If it is, increment the counter variable.
5. After the loop is complete, the counter variable will contain the number of occurrences of the string.

# Section 2: Using indexOf()

1. Initialize a counter variable to 0.
2. Use a while loop to iterate through the string.
3. Inside the loop, use the indexOf() method to get the index of the string you want to count.
4. If the index is greater than -1, increment the counter variable.
5. After the loop is complete, the counter variable will contain the number of occurrences of the string.

# Section 3: Using Regular Expression

1. Create a regular expression to match the string you want to count.
2. Use the match() method to find all the matches in the string.
3. The length of the returned array will be the number of occurrences of the string.

# Section 4: Using split()

1. Use the split() method to split the string into an array of substrings.
2. Use the filter() method to filter out all the substrings that don't match the string you want to count.
3. The length of the returned array will be the number of occurrences of the string.
