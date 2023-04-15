---
title: What is causing this to enter an endless cycle?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: This goes into an infinite loop in Java because the condition in the while loop never evaluates to false.
---

**Contents**

[TOC]

**Problem**
The following code goes into an infinite loop in Java:

```java
while (true) { 
    System.out.println("Hello World"); 
}
```

**Cause**
The code is an infinite loop because the condition of the while loop is always true. The loop will continue to execute until it is manually stopped or the program crashes.

**Solution**
To prevent the loop from running infinitely, a condition needs to be added to the while loop that will eventually become false. For example: 

```java
int i = 0;
while (i < 10) { 
    System.out.println("Hello World"); 
    i++;
}
```

**Conclusion**
In summary, the code goes into an infinite loop because the condition of the while loop is always true. To prevent the loop from running infinitely, a condition needs to be added to the while loop that will eventually become false.
