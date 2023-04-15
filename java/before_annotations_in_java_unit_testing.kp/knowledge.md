---
title: What are the distinctions between @before, @beforeclass, @beforeeach and @beforeall?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: @BeforeClass and @BeforeAll are used to execute code before all tests in a class, @Before and @BeforeEach are used to execute code before each test.
---

**Contents**

[TOC]

### @Before

`@Before` is a JUnit 4 annotation. It is used to run a method before each test. It is used to prepare the test environment before executing each test.

### @BeforeClass

`@BeforeClass` is a JUnit 4 annotation. It is used to run a method once before all tests in the class. It is used to perform time intensive activities, for example, to connect to a database.

### @BeforeEach

`@BeforeEach` is a JUnit 5 annotation. It is used to run a method before each test. It is used to prepare the test environment before executing each test.

### @BeforeAll

`@BeforeAll` is a JUnit 5 annotation. It is used to run a method once before all tests in the class. It is used to perform time intensive activities, for example, to connect to a database.
