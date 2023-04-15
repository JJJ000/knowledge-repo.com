---
title: Link to a method in another class using javadoc
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can link to a method in another class by using the fully qualified class name followed by the method name (e.g. `ClassName.methodName`).
---

**Contents**

[TOC]

### Link Syntax

The syntax for linking to a method in another class is:

`{@link packageName.ClassName#methodName()}`

### Example

For example, if you wanted to link to the `getName()` method in the `Person` class in the `com.example.people` package, you would use the following syntax:

`{@link com.example.people.Person#getName()}`

### Parameters

The syntax for linking to a method with parameters is:

`{@link packageName.ClassName#methodName(paramType1, paramType2, ...)}`

### Example

For example, if you wanted to link to the `addPerson(Person person)` method in the `People` class in the `com.example.people` package, you would use the following syntax:

`{@link com.example.people.People#addPerson(Person person)}`
