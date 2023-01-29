---
title: Split a Java string using a period (.)
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The String.split() method can be used to split a String object by a specified delimiter, in this case a dot (.).
---

**Contents**

[TOC]

1. **Creating the String**
To split a string with a dot, you must first create the string with the dot in it. You can do this by simply typing out the string and putting a dot in between the words. For example:
```
String str = "Hello.World";
```

2. **Using the Split Method**
To split the string, you can use the split() method. This method takes in a regular expression as an argument, and the dot (.) is a special character in regular expressions. So you must escape the dot with a backslash (\\) to indicate that it is a literal dot. The split() method will then split the string into an array of strings. For example:
```
String[] strArray = str.split("\\.");
```

3. **Accessing the Split Strings**
Once the string is split, you can access the individual strings by using the array index. For example:
```
String firstWord = strArray[0]; // "Hello"
String secondWord = strArray[1]; // "World"
```

4. **Example Output**
The output of the above code would be:
```
firstWord = "Hello"
secondWord = "World"
```
