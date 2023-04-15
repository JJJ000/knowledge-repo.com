---
title: Is it possible to capture more than one Java exception in a single catch block?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, you can catch multiple Java exceptions in the same catch clause by separating them with a pipe (|).
---

**Contents**

[TOC]

Yes

### Syntax

The syntax for catching multiple exceptions in one catch clause is as follows:

```java
try {
    // Code that might throw an exception
} catch (ExceptionType1 | ExceptionType2 | ExceptionType3 ex) {
    // Code to handle the exceptions
}
```

### Benefits

Catching multiple exceptions in one catch clause can be beneficial in certain situations. It can help reduce code duplication and make the code more concise. Additionally, it can help to make the code more readable by avoiding multiple nested catch blocks.

### Drawbacks

Catching multiple exceptions in one catch clause can also have some drawbacks. It can make debugging more difficult since it can be harder to determine which exception was thrown. Additionally, it can make the code less maintainable since any changes made to the catch block will affect all of the exceptions that are being caught.
