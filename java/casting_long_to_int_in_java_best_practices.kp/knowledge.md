---
title: Converting a long to an int in Java securely
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the `longValue()` method to safely cast a long to an int in Java.
---

**Contents**

[TOC]

**Casting Long to Int**

1. **Understanding the Range of Long and Int**
   Long is a 64-bit signed two's complement integer, while int is a 32-bit signed two's complement integer. This means that a long can store a much larger range of values than an int.

2. **Casting Long to Int**
   To safely cast a long to an int, the long must be within the range of an int. This means that the long must be between -2,147,483,648 and 2,147,483,647 (inclusive).

3. **Checking the Range**
   Before casting a long to an int, it is important to check that the long is within the range of an int. This can be done with a simple if statement:
   ```
   if (longValue >= Integer.MIN_VALUE && longValue <= Integer.MAX_VALUE) {
       int intValue = (int) longValue;
   }
   ```

4. **Catching Exceptions**
   If the long is not within the range of an int, an exception will be thrown. To catch this exception, a try-catch block should be used:
   ```
   try {
       int intValue = (int) longValue;
   } catch (Exception e) {
       // Handle exception
   }
   ```
