---
title: What is the best way to use mockito to create a list of a certain type?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Mockito can capture a list of specific type by using the ArgumentCaptor class.
---

**Contents**

[TOC]

### Setting Up the Mocks

To capture a list of a specific type with Mockito, you will need to create a mock of the list and set the type of the list elements. To do this, you can use the `Mockito.mock(List.class, Mockito.withSettings().extraInterfaces(MyType.class))` method. This will create a mock of the list with the specified type for the list elements.

### Capturing the List

Once the mock is set up, you can capture the list by using the `Mockito.capture(List.class)` method. This will capture the list and return it as a `List<MyType>`, where `MyType` is the type you specified when creating the mock.

### Verifying the List

After capturing the list, you can use Mockito's `verify()` method to verify that the list contains the expected elements. For example, you can use the `Mockito.verify(list).contains(expectedElement)` method to verify that the list contains the expected element.

### Asserting the List

Finally, you can use Mockito's `assertThat()` method to assert that the list contains the expected elements. For example, you can use the `Mockito.assertThat(list, Matchers.hasItem(expectedElement))` method to assert that the list contains the expected element.
