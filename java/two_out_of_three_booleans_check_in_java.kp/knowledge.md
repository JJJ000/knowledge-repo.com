---
title: Determine if two or more of the three booleans are true
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, you can use the logical OR operator (||) to check if at least two out of three booleans are true.
---

**Contents**

[TOC]

### Using if-else statement

```
if (boolean1 == true && boolean2 == true)
    System.out.println("At least two booleans are true");
else if (boolean1 == true && boolean3 == true)
    System.out.println("At least two booleans are true");
else if (boolean2 == true && boolean3 == true)
    System.out.println("At least two booleans are true");
else
    System.out.println("Less than two booleans are true");
```

### Using Logical Operators

```
if ((boolean1 && boolean2) || (boolean1 && boolean3) || (boolean2 && boolean3))
    System.out.println("At least two booleans are true");
else
    System.out.println("Less than two booleans are true");
```

### Using Bitwise Operators

```
int result = (boolean1 ? 1 : 0) + (boolean2 ? 1 : 0) + (boolean3 ? 1 : 0);
if (result >= 2)
    System.out.println("At least two booleans are true");
else
    System.out.println("Less than two booleans are true");
```

### Using Array

```
boolean[] booleans = {boolean1, boolean2, boolean3};
int count = 0;
for (boolean b : booleans) {
    if (b)
        count++;
}
if (count >= 2)
    System.out.println("At least two booleans are true");
else
    System.out.println("Less than two booleans are true");
```
