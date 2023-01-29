---
title: Generating random numbers in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Random numbers can be generated in Java using the Math.random() method.
---

**Contents**

[TOC]

### Math.random()
Math.random() is a static method of the Math class that returns a pseudorandom double type number greater than or equal to 0.0 and less than 1.0.

### Example
The following example uses Math.random() to generate a random number and print it to the console.

```
public class RandomNumber {
    public static void main(String[] args) {
        double randomNumber = Math.random();
        System.out.println("Random number: " + randomNumber);
    }
}
```

### Generating a Range
To generate a random number within a specific range, the following formula can be used:

```
double randomNumber = lowerBound + (Math.random() * (upperBound - lowerBound));
```

### Example
The following example uses the formula above to generate a random number between 1 and 10 and print it to the console.

```
public class RandomNumberRange {
    public static void main(String[] args) {
        double lowerBound = 1;
        double upperBound = 10;
        double randomNumber = lowerBound + (Math.random() * (upperBound - lowerBound));
        System.out.println("Random number: " + randomNumber);
    }
}
```
