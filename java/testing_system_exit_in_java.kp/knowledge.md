---
title: How can I test Java methods that use system.exit()?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use a mocking framework to mock the System.exit() method and return a specific value.
---

**Contents**

[TOC]

#1 Using a Security Manager
A SecurityManager can be used to prevent a call to System.exit() from actually exiting the JVM. This can be done by registering a custom SecurityManager that overrides the checkExit() method.

#2 Using a Custom Assertion
A custom assertion can be used to simulate a call to System.exit(). This can be done by creating an assertion that checks to see if the method under test calls System.exit(). If it does, the assertion can throw an exception which will cause the test to fail.

#3 Using a Mock Object
A mock object can be used to simulate a call to System.exit(). This can be done by creating a mock object that wraps the System class and overrides the exit() method. The mock object can then be used to check to see if the method under test calls System.exit().

#4 Using a Test Framework
Many test frameworks have built-in support for testing methods that call System.exit(). For example, JUnit has an @Test(expected=SystemExitException.class) annotation that can be used to test methods that call System.exit(). This annotation will cause the test to fail if the method under test calls System.exit().
