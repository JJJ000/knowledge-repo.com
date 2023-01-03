---
title: What is the method for generating random integers within a specified range in Java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-03 00:00:00
updated_at: 2023-01-03 00:00:00
tldr: You can use the `nextInt` method of the `java.util.Random` class to generate a random integer within a specific range.
---

**Contents**

[TOC]


Here are the steps for generating a random integer within a specific range in Java:

### Step 1: Import the java.util.Random class

```Java
import java.util.Random;
```

### Step 2: Create a new Random object

```Java
Random random = new Random();
```

### Step 3: Set the range for the random integers

```Java
int min = 10;
int max = 20;
```

### Step 4: Generate a random integer within the range

```Java
int randomInt = random.nextInt((max - min) + 1) + min;
```

Here's the code that puts these steps together:

```Java
import java.util.Random;

public class Main {
  public static void main(String[] args) {
    // Step 1: Import the java.util.Random class
    // Step 2: Create a new Random object
    Random random = new Random();
    
    // Step 3: Set the range for the random integers
    int min = 10;
    int max = 20;
    
    // Step 4: Generate a random integer within the range
    int randomInt = random.nextInt((max - min) + 1) + min;
    
    System.out.println(randomInt);
  }
}
```
