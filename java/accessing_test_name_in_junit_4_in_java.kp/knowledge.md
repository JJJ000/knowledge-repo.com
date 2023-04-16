---
title: Find the name of the test being run in junit 4
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The name of the currently executing test in JUnit 4 in Java can be obtained using the getName() method of the TestCase class.
---

**Contents**

[TOC]

# Solution

## Using the `Description` Class

The `Description` class provides information about the currently executing test. It can be accessed by overriding the `Description` method in the `org.junit.runner.Description` class. The `getDisplayName()` method of the `Description` class can be used to get the name of the currently executing test.

## Example

Below is an example of how to use the `Description` class to get the name of the currently executing test.

```java
@Override
public Description getDescription() {
    Description description = super.getDescription();
    String testName = description.getDisplayName();
    System.out.println("Currently executing test: " + testName);
    return description;
}
```

## Considerations

It is important to note that the `Description` class can only be used in JUnit 4, as JUnit 5 and later versions use a different approach to accessing test information.
