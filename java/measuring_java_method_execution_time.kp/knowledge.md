---
title: Determine how long it takes for a Java method to run
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To measure execution time for a Java method, use the System.nanoTime() method.
---

**Contents**

[TOC]

### Using System.nanoTime() 

System.nanoTime() is a method that is used to measure the execution time of a Java method. It returns the current value of the most precise available system timer, in nanoseconds.

### Steps

1. Create a variable to store the start time before the method is executed:

```java
long startTime = System.nanoTime();
```

2. Execute the method.

3. Create a variable to store the end time after the method is executed:

```java
long endTime = System.nanoTime();
```

4. Calculate the difference between the start and end times:

```java
long elapsedTime = endTime - startTime;
```

5. Convert the elapsed time from nanoseconds to milliseconds:

```java
long elapsedTimeInMillis = TimeUnit.NANOSECONDS.toMillis(elapsedTime);
```

6. Print the elapsed time in milliseconds:

```java
System.out.println("Execution time in milliseconds: " + elapsedTimeInMillis);
```
