---
title: What is the best way to create a random number within a certain range in android?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can generate a random number in a specific range in Android using the Java method Math.random() and multiplying it by the desired range.
---

**Contents**

[TOC]

1. Using `Math.random()` Method
--------------------------------
The `Math.random()` method can be used to generate a random number within a specific range. This method returns a double value with a positive sign, greater than or equal to 0.0 and less than 1.0.

To generate a random number within a range, use the following code:

```java
int min = 10;
int max = 20;
int randomNumber = (int)(Math.random() * (max - min + 1)) + min;
```

2. Using `Random` Class
-----------------------
The `Random` class of the `java.util` package can also be used to generate random numbers. To generate a random number within a range, use the following code:

```java
int min = 10;
int max = 20;
Random random = new Random();
int randomNumber = random.nextInt((max - min) + 1) + min;
```

3. Using `SecureRandom` Class
-----------------------------
The `SecureRandom` class of the `java.security` package can also be used to generate random numbers. To generate a random number within a range, use the following code:

```java
int min = 10;
int max = 20;
SecureRandom random = new SecureRandom();
int randomNumber = random.nextInt((max - min) + 1) + min;
```

4. Using `ThreadLocalRandom` Class
----------------------------------
The `ThreadLocalRandom` class of the `java.util.concurrent` package can also be used to generate random numbers. To generate a random number within a range, use the following code:

```java
int min = 10;
int max = 20;
ThreadLocalRandom random = ThreadLocalRandom.current();
int randomNumber = random.nextInt((max - min) + 1) + min;
```
