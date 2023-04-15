---
title: What is the process for verifying that no exceptions are thrown?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use a try-catch block to test that no exception is thrown in Java.
---

**Contents**

[TOC]

### Creating a Test Case

When testing that no exception is thrown in Java, the first step is to create a test case. This involves writing code that will be executed in order to determine whether or not an exception is thrown. The code should be written in such a way that it is likely to throw an exception if one is present. This can be done by deliberately introducing a bug into the code or by using a method that is known to throw an exception.

### Running the Test Case

Once the test case has been written, it should be run in order to determine whether or not an exception is thrown. This can be done by executing the code in a debugger or by running the code in an environment where exceptions are logged. It is important to make sure that the code is run in a variety of different scenarios in order to ensure that any potential exceptions are caught.

### Checking the Results

After the test case has been run, the results should be checked to determine whether or not an exception was thrown. If an exception was thrown, the cause should be identified and the code should be corrected in order to prevent the exception from occurring again. If no exception was thrown, then the test case has been successful and the code can be considered to be free of exceptions.

### Documenting the Results

Finally, the results of the test should be documented in order to ensure that any future changes to the code do not introduce an exception. This documentation should include the code that was used to test for exceptions, the results of the test, and any corrective actions that were taken. This documentation will help to ensure that any future changes to the code do not introduce an unexpected exception.
