---
title: What is the best way to check that a particular method was not invoked using mockito?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use Mockito`s verifyNoInteractions() method to verify that a specific method was not called.
---

**Contents**

[TOC]

### Solution

### 1. Mock the Method
First, mock the method you want to verify has not been called. This can be done using the `Mockito.mock()` method. For example, if you want to verify that a method called `foo()` was not called, you would mock it like so:

```java
Foo mockFoo = Mockito.mock(Foo.class);
```

### 2. Use Mockito.never()
Next, use the `Mockito.never()` method to verify that the method was not called. This method takes the mocked object as an argument and returns a `VerificationMode` object. For example:

```java
Mockito.never().verify(mockFoo);
```

### 3. Use Mockito.verify()
Finally, use the `Mockito.verify()` method to verify that the method was not called. This method takes the mocked object and a `VerificationMode` object as arguments. For example:

```java
Mockito.verify(mockFoo, Mockito.never());
```

### 4. Assertion
To complete the verification, you can use an assertion to check that the verification was successful. For example:

```java
Assert.assertTrue(Mockito.verify(mockFoo, Mockito.never()));
```
