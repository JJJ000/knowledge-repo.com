---
title: Check if a Java string consists solely of numerical characters and no letters
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the String method matches() with the regular expression `[0-9]+` to check if a String contains only numbers.
---

**Contents**

[TOC]

1. ## Using Regular Expressions

To check if a string contains only numbers and not letters, you can use a regular expression to check for any non-numeric characters in the string.

```
String str = "12345";
if (str.matches("[0-9]+")) {
    System.out.println("String contains only numbers.");
} else {
    System.out.println("String contains letters or other characters.");
}
```

2. ## Using a Character Iterator

Another way to check if a string contains only numbers and not letters is to use a character iterator to iterate through each character in the string and check if it is a number or not.

```
String str = "12345";
boolean isNumeric = true;
for (int i = 0; i < str.length(); i++) {
    char c = str.charAt(i);
    if (!Character.isDigit(c)) {
        isNumeric = false;
        break;
    }
}
if (isNumeric) {
    System.out.println("String contains only numbers.");
} else {
    System.out.println("String contains letters or other characters.");
}
```

3. ## Using the String API

The Java String API also provides a method to check if a string contains only numbers and not letters. The `String.matches()` method can be used to check if the string contains only numbers.

```
String str = "12345";
if (str.matches("-?\\d+(\\.\\d+)?")) {
    System.out.println("String contains only numbers.");
} else {
    System.out.println("String contains letters or other characters.");
}
```

4. ## Using a Loop

Finally, you can also use a loop to iterate through each character in the string and check if it is a number or not.

```
String str = "12345";
boolean isNumeric = true;
for (int i = 0; i < str.length(); i++) {
    char c = str.charAt(i);
    if (!Character.isDigit(c)) {
        isNumeric = false;
        break;
    }
}
if (isNumeric) {
    System.out.println("String contains only numbers.");
} else {
    System.out.println("String contains letters or other characters.");
}
```
