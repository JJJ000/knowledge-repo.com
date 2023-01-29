---
title: How can I loop through each character in a Java string?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The easiest and most correct way to iterate through the characters of a string in Java is to use a for loop with the String`s charAt() method.
---

**Contents**

[TOC]

### Using a For Loop

The most common and straightforward way to iterate through the characters of a string in Java is to use a for loop. The syntax for this is as follows:

```java
String str = "Hello World!";
for(int i = 0; i < str.length(); i++) {
    char c = str.charAt(i);
    // do something with the character c
}
```

This loop will iterate through each character in the string, starting from the first character and ending with the last character. The `charAt(i)` method will return the character at the given index in the string.

### Using a For-Each Loop

Another way to iterate through the characters of a string in Java is to use a for-each loop. The syntax for this is as follows:

```java
String str = "Hello World!";
for(char c : str.toCharArray()) {
    // do something with the character c
}
```

This loop will iterate through each character in the string, starting from the first character and ending with the last character. The `toCharArray()` method will return an array of characters that can be iterated over using the for-each loop.

### Using a Stream

A third way to iterate through the characters of a string in Java is to use a stream. The syntax for this is as follows:

```java
String str = "Hello World!";
str.chars().forEach(c -> {
    // do something with the character c
});
```

This loop will iterate through each character in the string, starting from the first character and ending with the last character. The `chars()` method will return a stream of characters that can be iterated over using the forEach method.
