---
title: What is the distinction between @mock, @mockbean and mockito.mock() in mockito?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: @Mock is used to create a mock object for a given class, @MockBean is used to create a mock bean for a given class in a Spring application context, and Mockito.mock() is used to create a generic mock object for a given class.
---

**Contents**

[TOC]

### Mockito.mock()
Mockito.mock() is a static method of the Mockito class. It is used to create a mock object of a given class or interface. It takes a class or interface as an argument and returns an instance of a mock object for that class or interface. It is used to create mock objects for unit testing.

### @Mock
@Mock is an annotation provided by Mockito. It is used to create a mock object of a given class or interface. It is used to create mock objects for unit testing.

### @MockBean
@MockBean is an annotation provided by Spring Boot. It is used to create a mock object of a given class or interface and register it as a bean in the Spring application context. It is used to create mock objects for integration testing.
