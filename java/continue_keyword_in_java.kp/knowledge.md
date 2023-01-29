---
title: Can you explain the purpose of the "continue" keyword and how it is used in Java programming?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The `continue` keyword is used to skip the current iteration of a loop and move on to the next one in Java.
---

**Contents**

[TOC]

#Definition
The `continue` keyword is a Java statement that causes the flow of control to skip the current iteration of a loop and continue with the next iteration.

#Syntax
The syntax for `continue` is:
```
continue;
```

#Usage
`continue` can be used in any loop statement, such as `for`, `while`, and `do-while` loops. It can be used to skip certain iterations of the loop, such as when a certain condition is not met.

#Example
For example, the following code will print only the even numbers from 0 to 10:
```
for (int i=0; i<10; i++) {
    if (i % 2 != 0) {
        continue;
    }
    System.out.println(i);
}
```
The output of this code will be:
```
0
2
4
6
8
10
```
