---
title: What is the process for creating a random alphanumeric sequence?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-23 00:00:00
updated_at: 2023-01-23 00:00:00
tldr: A random alpha-numeric string can be generated in Java by using the Random class and its `nextInt()` method to generate random numbers and combining them with characters from the ASCII character set.
---

**Contents**

[TOC]

### Import Random Class

In order to generate a random alpha-numeric string in Java, we must first import the Random class. This is done by using the following code:

```java
import java.util.Random;
```

### Generate Random Characters

Once the Random class has been imported, we can use it to generate random characters. We can do this by creating a new Random object and then using the `nextInt()` method to generate a random integer between 0 and 9. We can then add the corresponding character to a StringBuilder object. This can be done with the following code:

```java
Random random = new Random();
StringBuilder sb = new StringBuilder();
for (int i = 0; i < 10; i++) {
    int randomInt = random.nextInt(10);
    char randomChar = (char)('0' + randomInt);
    sb.append(randomChar);
}
```

### Generate Random Alphabets

In order to generate random alphabets, we can use the same approach as before but with a different range of integers. Instead of using 0 to 9, we can use 65 to 90 to generate a random alphabet. This can be done with the following code:

```java
Random random = new Random();
StringBuilder sb = new StringBuilder();
for (int i = 0; i < 10; i++) {
    int randomInt = random.nextInt(26) + 65;
    char randomChar = (char)(randomInt);
    sb.append(randomChar);
}
```

### Combine Characters and Alphabets

Once we have generated both the random characters and alphabets, we can combine them to form a random alpha-numeric string. This can be done by simply combining the two StringBuilder objects into a single String. This can be done with the following code:

```java
String randomString = sb1.toString() + sb2.toString();
```
