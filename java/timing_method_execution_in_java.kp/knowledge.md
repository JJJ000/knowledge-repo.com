---
title: What is the best way to measure the amount of time it takes for a method to execute in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use System.nanoTime() before and after the method to calculate the execution time.
---

**Contents**

[TOC]

### Using System.nanoTime()

The `System.nanoTime()` method can be used to time the execution of a method in Java. This method returns the current value of the most precise available system timer, in nanoseconds. To time a method, one must call `System.nanoTime()` before and after the method call, and then subtract the starting time from the ending time to determine the total execution time.

For example:

```java
long startTime = System.nanoTime();
// Method call
long endTime = System.nanoTime();
long duration = (endTime - startTime);
```

### Using Stopwatch

The `Stopwatch` class from the Apache Commons Lang library can also be used to time the execution of a method. This class provides a convenient API for measuring elapsed time in nanoseconds. To time a method, one must create a `Stopwatch` instance, call the `start()` method, then call the method to be timed, and finally call the `stop()` method. The elapsed time can then be obtained using the `getTime()` method.

For example:

```java
Stopwatch stopwatch = new Stopwatch();
stopwatch.start();
// Method call
stopwatch.stop();
long duration = stopwatch.getTime();
```

### Using Profiler

The Java Virtual Machine (JVM) provides a profiler which can be used to measure the execution time of a method. This profiler is enabled by passing the `-prof` flag when starting the JVM. Once enabled, the profiler will measure the execution time of each method and report the results in a file.

For example:

```
java -prof MyClass
```

This will generate a `java.prof` file which contains the execution time of each method. The profiler can also be used to measure the memory usage of each method.
