---
title: What is the method for retrieving the final character of a string?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the String.charAt() method to get the last character of a string in Java.
---

**Contents**

[TOC]

#### Using the charAt() Method

The charAt() method can be used to get the last character of a string in Java. The syntax for the charAt() method is as follows:

`string.charAt(string.length()-1)`

The charAt() method takes an integer as an argument and returns the character at the specified index in the string. In this case, the index is the length of the string minus one, which will return the last character of the string.

#### Using the substring() Method

The substring() method can also be used to get the last character of a string in Java. The syntax for the substring() method is as follows:

`string.substring(string.length()-1, string.length())`

The substring() method takes two integers as arguments and returns the substring starting from the first integer index up to, but not including, the second integer index. In this case, the first integer is the length of the string minus one, and the second integer is the length of the string, which will return the last character of the string.

#### Using the StringBuilder Class

The StringBuilder class can also be used to get the last character of a string in Java. The syntax for the StringBuilder class is as follows:

`StringBuilder sb = new StringBuilder(string);`
`char lastChar = sb.charAt(sb.length()-1);`

The StringBuilder class takes a string as an argument and creates a StringBuilder object with the string passed in. The charAt() method can then be used to get the last character of the string. The charAt() method takes an integer as an argument and returns the character at the specified index in the StringBuilder object. In this case, the index is the length of the StringBuilder object minus one, which will return the last character of the string.
