---
title: What is the method for capitalizing the first letter of a string in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the String.substring() and String.toUpperCase() methods to capitalize the first letter of a String in Java.
---

**Contents**

[TOC]

### Using String.substring()

1. Retrieve the first character of the String using `String.substring()`:
    ```
    String firstChar = str.substring(0, 1);
    ```
2. Convert the retrieved character to upper case using `Character.toUpperCase()`:
    ```
    firstChar = Character.toUpperCase(firstChar);
    ```
3. Concatenate the uppercase character to the rest of the String using `String.substring()`:
    ```
    str = firstChar + str.substring(1);
    ```

### Using StringBuilder

1. Create a `StringBuilder` object from the String:
    ```
    StringBuilder sb = new StringBuilder(str);
    ```
2. Retrieve the first character of the String using `StringBuilder.charAt()`:
    ```
    char firstChar = sb.charAt(0);
    ```
3. Convert the retrieved character to upper case using `Character.toUpperCase()`:
    ```
    firstChar = Character.toUpperCase(firstChar);
    ```
4. Replace the first character with the uppercase character using `StringBuilder.setCharAt()`:
    ```
    sb.setCharAt(0, firstChar);
    ```
5. Get the modified String using `StringBuilder.toString()`:
    ```
    str = sb.toString();
    ```
