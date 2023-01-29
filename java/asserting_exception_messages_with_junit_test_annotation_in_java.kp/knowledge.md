---
title: What is the syntax for using junit test annotation to assert an exception message?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can use the @Test(expected = Exception.class) annotation to assert an expected exception message with JUnit in Java.
---

**Contents**

[TOC]

### Step 1: Prepare the Test

Before you can assert an exception message with JUnit Test, you must first create the test. To do this, you will need to create a class that extends the `org.junit.Test` annotation. Inside the class, you will need to create a method that will contain the code that you wish to test.

### Step 2: Throw the Exception

Once you have created your test, you will need to throw the exception that you wish to test. This can be done by using the `throw` keyword in Java. Inside the method, you will need to create an instance of the exception that you wish to throw and then use the `throw` keyword to throw the exception.

### Step 3: Assert the Exception

Once you have thrown the exception, you will need to assert the exception message. This can be done by using the `@Test` annotation and specifying the expected exception type. In the annotation, you will need to specify the expected exception type and the expected message.

### Step 4: Run the Test

Once you have created the test and asserted the exception message, you will need to run the test. This can be done by running the test class with the `junit` command. If the test passes, then the exception message will be asserted correctly.
