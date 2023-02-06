---
title: Substituting all symbols that are not letters or numbers with nothing
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: String.replaceAll(`[^A-Za-z0-9]`, ``)
---

**Contents**

[TOC]

##### Using Regular Expressions

We can use the `replaceAll()` method of the `String` class in Java to replace all non-alphanumeric characters with empty strings. This method takes in a regular expression as an argument. The following code snippet shows how this can be done:

```
String str = "Hello, World!";
str = str.replaceAll("[^A-Za-z0-9]", "");
System.out.println(str);
```

The output of the above code will be:

`HelloWorld`

##### Using for Loop

We can also use a for loop to iterate over the characters of the string and check for alphanumeric characters. If the character is not alphanumeric, we can replace it with an empty string. The following code snippet shows how this can be done:

```
String str = "Hello, World!";
StringBuilder sb = new StringBuilder();

for (int i = 0; i < str.length(); i++) {
    char c = str.charAt(i);
    if (Character.isLetterOrDigit(c)) {
        sb.append(c);
    }
}

String newStr = sb.toString();
System.out.println(newStr);
```

The output of the above code will be:

`HelloWorld`
