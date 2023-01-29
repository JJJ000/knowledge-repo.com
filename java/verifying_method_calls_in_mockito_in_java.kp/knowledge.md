---
title: How can mockito be used to confirm that a method was invoked on an object created inside a different method?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can use Mockito`s verify() method to verify that a method was called on an object created within a method.
---

**Contents**

[TOC]

1. Preparing for Verification
--------------------------------
Before attempting to verify that a method was called on an object created within a method, it is important to ensure that the object is accessible to the test. This can be done by using a `Mockito.spy()` to wrap the object. This will allow the object to be used and monitored without changing the existing code.

2. Verifying Method Calls
-------------------------
Once the object is accessible, `Mockito.verify()` can be used to verify that a method was called on the object. This can be done by passing the `Mockito.verify()` method the object, the method name, and any parameters that are required.

3. Using Argument Captors
-------------------------
If the method being called requires parameters, `Mockito.ArgumentCaptor` can be used to capture the arguments passed to the method. This will allow the test to verify that the correct arguments were passed to the method.

4. Verifying Multiple Calls
---------------------------
If the method needs to be called multiple times, `Mockito.times()` can be used to specify the number of times the method should be called. This will ensure the method is called the correct number of times.
