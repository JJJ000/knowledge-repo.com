---
title: What is the best way to make a mockito mock object return a different value on subsequent calls?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Mockito`s `when` method can be used to specify the desired return value for a mock object each time it is called.
---

**Contents**

[TOC]

# Section 1: Setting the Mock Object

To tell a Mockito mock object to return something different the next time it is called, you must first create a mock object. This can be done using the Mockito.mock() method.

# Section 2: Setting the Return Value

Once the mock object has been created, you can set the return value using the Mockito.when() and thenReturn() methods. The when() method takes the method to be mocked as an argument, and thenReturn() takes the value to be returned.

# Section 3: Setting the New Return Value

To set a new return value for the same mock object, you can use the same when() and thenReturn() methods. However, this time you must use the Mockito.doReturn() method instead of the thenReturn() method. This allows you to set a new return value for the same mock object.

# Section 4: Verifying the Return Value

Finally, to verify that the mock object is returning the expected value, you can use the Mockito.verify() method. This allows you to check that the mock object is returning the expected value each time it is called.
