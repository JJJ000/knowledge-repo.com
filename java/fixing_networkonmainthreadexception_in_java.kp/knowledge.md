---
title: What steps do I need to take to resolve the 'android.os.networkonmainthreadexception' error?
authors:
- nanja_dev
tags:
- android
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use an AsyncTask or other thread to perform network operations.
---

**Contents**

[TOC]

### Section 1 - Understand the Exception
The `android.os.NetworkOnMainThreadException` is a runtime exception thrown when an application attempts to perform a network operation on the main thread of its process. This is a common mistake in Android development and should be avoided as much as possible.

### Section 2 - Identify the Problem
The problem is that the application is attempting to perform a network operation on the main thread, which is not allowed. This is because the main thread is responsible for handling UI events and should not be blocked with long-running tasks.

### Section 3 - Solution
The solution is to move the network operation to a background thread. This can be done using the `AsyncTask` class or by using a `Thread` and `Handler` combination.

### Section 4 - Implement the Solution
Once the background thread has been created, the network operation can be moved to it. This can be done by simply creating a new `Runnable` and passing it to the thread. The `Runnable` should contain the code for the network operation and should be executed on the background thread.
