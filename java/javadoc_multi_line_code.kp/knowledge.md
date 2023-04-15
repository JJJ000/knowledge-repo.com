---
title: An example of multiple lines of code in a javadoc comment
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A Javadoc comment example can include multiple lines of code preceded by an asterisk (*) on each line.
---

**Contents**

[TOC]

### Section 1

```java
/**
 * This method does something
 *
 * @param foo the value of foo
 * @param bar the value of bar
 */
public void doSomething(int foo, int bar) {
    // Do Something
}
```

### Section 2

```java
/**
 * This method does something else
 *
 * @param baz the value of baz
 * @param qux the value of qux
 */
public void doSomethingElse(int baz, int qux) {
    // Do Something Else
}
```

### Section 3

```java
/**
 * This method combines the two methods
 *
 * @param foo the value of foo
 * @param bar the value of bar
 * @param baz the value of baz
 * @param qux the value of qux
 */
public void doSomethingCombined(int foo, int bar, int baz, int qux) {
    doSomething(foo, bar);
    doSomethingElse(baz, qux);
}
```

### Section 4

```java
/**
 * This method does something with a boolean value
 *
 * @param foo the value of foo
 * @param bar the value of bar
 * @param flag a boolean value
 */
public void doSomethingWithFlag(int foo, int bar, boolean flag) {
    if (flag) {
        doSomething(foo, bar);
    } else {
        doSomethingElse(foo, bar);
    }
}
```
