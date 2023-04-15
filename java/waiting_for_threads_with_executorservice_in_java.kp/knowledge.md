---
title: What is the best way to ensure that all threads finish executing when using an executorservice?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the ExecutorService`s shutdown() method and awaitTermination() method to wait for all threads to finish.
---

**Contents**

[TOC]

### Create an ExecutorService

The first step to waiting for all threads to finish using ExecutorService in Java is to create an ExecutorService. This can be done in a few different ways, depending on the desired behavior. 

If the goal is to create a fixed thread pool, the Executors class provides a static method for doing so:

```java
ExecutorService executor = Executors.newFixedThreadPool(nThreads);
```

Where nThreads is the desired number of threads.

Alternatively, if the goal is to create a cached thread pool, the Executors class provides a static method for doing so:

```java
ExecutorService executor = Executors.newCachedThreadPool();
```

### Submit Tasks

Once an ExecutorService has been created, tasks can be submitted to it for execution. This can be done using the submit() method, which takes a Runnable or Callable task as an argument:

```java
Future<?> future = executor.submit(task);
```

### Shutdown the ExecutorService

Once all tasks have been submitted, the ExecutorService must be shutdown in order to wait for all threads to finish. This can be done using the shutdown() method:

```java
executor.shutdown();
```

### Wait for Termination

Finally, the program must wait for the ExecutorService to terminate. This can be done using the awaitTermination() method, which takes a timeout value as an argument:

```java
executor.awaitTermination(timeout, TimeUnit.SECONDS);
```

Where timeout is the desired timeout value in seconds.
