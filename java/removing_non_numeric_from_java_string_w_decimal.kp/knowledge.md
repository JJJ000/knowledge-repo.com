---
title: Remove all non-numeric characters from a Java string, except for the decimal point
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the replaceAll() method with a regex pattern to replace all non-numeric characters with an empty string, but keep the decimal separator.
---

**Contents**

[TOC]

**Section 1: Understanding the Problem**

The goal of this problem is to take a String and remove all non-numeric characters, but keep the decimal separator (if present). 

**Section 2: Breaking Down the Solution**

To solve this problem, we need to: 
1. Iterate over the characters in the String. 
2. Check if the character is a non-numeric character. 
3. If it is, remove it from the String. 
4. If it is a decimal separator, keep it in the String. 

**Section 3: Writing the Code**

We can use a `for` loop to iterate over the characters in the String. We can then use an `if` statement to check if the character is a non-numeric character. If it is, we can use the `String.replace()` method to remove it from the String. Finally, we can use an `else` statement to keep the decimal separator in the String. 

**Section 4: Testing the Code**

We can test the code by providing a test String and checking if the output is correct. For example, if we provide the String `"abc123.45def"`, the output should be `"123.45"`.
