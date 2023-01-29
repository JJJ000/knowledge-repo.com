---
title: What is the process for unit testing abstract classes by using stubs for extension?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Create a concrete subclass of the abstract class and use stubs to override any abstract methods that need to be tested.
---

**Contents**

[TOC]

### Create a Stub

The first step to unit testing an abstract class is to create a stub. A stub is a class that extends the abstract class and provides dummy implementations for the abstract methods. This allows the abstract class to be instantiated and tested in isolation.

### Implement the Abstract Methods

Next, the stub needs to implement the abstract methods. This can be done by providing dummy implementations that simply return a predetermined value. This allows the abstract class to be tested without needing to implement any real logic.

### Test the Abstract Class

Once the stub has been created, the abstract class can then be tested. This can be done by instantiating the stub and calling the methods of the abstract class. The results of the calls can then be verified to ensure the abstract class is functioning correctly.

### Assert the Results

The final step is to assert the results of the tests. This can be done by using an assertion library such as JUnit or TestNG. This allows the results of the tests to be verified and any errors to be reported.
