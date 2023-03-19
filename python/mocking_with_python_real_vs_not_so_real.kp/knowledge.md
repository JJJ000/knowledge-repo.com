---
title: Comparison between mock and magicmock
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Mock is used for basic mocking, while MagicMock is used for more advanced mocking techniques such as returning specific values or raising exceptions.
---

**Contents**

[TOC]

# Overview

Mock and MagicMock are two different classes in Python used for testing. They both mimic objects or functions, but with different behaviors. In this section, we will provide an overview of both classes.

## Mock 

Mock is a class provided by the unittest.mock module. It is used to mock objects or functions and their responses. Mock objects can be created manually or by calling the `unittest.mock.Mock()` method. When a mock object is created, you can assign attributes to it and set its return values. 

## MagicMock 

MagicMock is a subclass of Mock. It has all the functions of Mock, but with some extra features. In addition to the attributes and return values that can be set with Mock, MagicMock has default return values for all possible calls. This means that it can be used without setting return values for every possible call that could be made to the object.

# Differences

While both Mock and MagicMock are used for testing, they have some differences. In this section, we will highlight some of the differences between the two.

## Return values

Mock objects do not have a default return value for every possible call that could be made to them. You need to specify the return value for every call made to the object. MagicMock, on the other hand, has default return values for all possible calls. 

## Functionality

Mock and MagicMock have the same functionality, but MagicMock has some additional features. For example, MagicMock provides a wrapper function that can be used to create a new mock object with the same default behavior.

## Performance

Mock is faster than MagicMock. This is because MagicMock needs to have a default return value for every possible call that could be made to it. As a result, MagicMock can take longer to create objects than Mock.

# Use Cases

Both Mock and MagicMock can be used in a variety of testing scenarios. In this section, we will highlight some use cases for both classes.

## Mock

Mock objects can be used in testing code that interacts with other objects, such as databases or APIs. They can also be used to test functions that have side effects. By mocking the objects or functions that have side effects, you can ensure that the code being tested behaves correctly.

## MagicMock

MagicMock is useful when you want to automate the creation of mock objects with default behaviors. This can save time because you do not have to set up return values for every possible call that could be made to the object. MagicMock is also useful when you want to create a mock object with a large number of pre-defined behaviors. This can help simplify your testing code.
