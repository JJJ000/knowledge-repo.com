---
title: I am receiving a "nosuchmethoderror org.hamcrest.matcher.describemismatch" error when running tests in intellij 10.5
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: This error is caused by an outdated version of the Hamcrest library.
---

**Contents**

[TOC]

# Overview
NoSuchMethodError: org.hamcrest.Matcher.describeMismatch is an error that occurs when running a test in IntelliJ 10.5 in Java. It occurs when a method is not found in the class that is being tested.

# Cause
This error is caused by the lack of the describeMismatch method in the org.hamcrest.Matcher class. The describeMismatch method was added in version 1.3 of the Hamcrest library, but IntelliJ 10.5 uses version 1.2.

# Solution
To fix this error, you need to upgrade the version of the Hamcrest library used by IntelliJ 10.5. To do this, you can add the latest version of the Hamcrest library to the classpath of your project.

# Conclusion
NoSuchMethodError: org.hamcrest.Matcher.describeMismatch is an error that occurs when running a test in IntelliJ 10.5 in Java. It is caused by the lack of the describeMismatch method in the org.hamcrest.Matcher class. To fix this error, you need to upgrade the version of the Hamcrest library used by IntelliJ 10.5.
