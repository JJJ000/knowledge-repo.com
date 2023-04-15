---
title: An unsupportedtemporaltypeexception is thrown when attempting to format an instant object to a string
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: UnsupportedTemporalTypeException is thrown when an unsupported field is used in an Instant formatting operation.
---

**Contents**

[TOC]

### Overview
UnsupportedTemporalTypeException is an unchecked exception thrown when an unsupported field is accessed in a temporal object. This exception is thrown when an application attempts to format an Instant object to a String using a formatter that does not support the Instant class.

### Cause
The UnsupportedTemporalTypeException is thrown when an application attempts to format an Instant object to a String using a formatter that does not support the Instant class. The Instant class represents an instantaneous point on the time-line. It does not have any fields, such as year, month, day, hour, minute, second, and so on. Therefore, a formatter that does not support the Instant class will throw an UnsupportedTemporalTypeException.

### Solution
To solve this problem, you can use a formatter that supports the Instant class. The DateTimeFormatter class provides a formatter that supports the Instant class. The following code snippet shows how to use the DateTimeFormatter to format an Instant object to a String:

```java
Instant instant = Instant.now();
DateTimeFormatter formatter = DateTimeFormatter.ISO_INSTANT;
String formattedInstant = formatter.format(instant);
```

### Conclusion
The UnsupportedTemporalTypeException is thrown when an application attempts to format an Instant object to a String using a formatter that does not support the Instant class. To solve this problem, you can use a formatter that supports the Instant class, such as the DateTimeFormatter class.
