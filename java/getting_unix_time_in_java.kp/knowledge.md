---
title: Obtaining the unix timestamp in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: In Java, you can use the Instant class from the java.time package to get the current unixtime.
---

**Contents**

[TOC]

1. **Importing the Necessary Libraries**

In order to use the unixtime in Java, we need to import the necessary libraries. The most important of these is the Java Date class, which is used to store and manipulate dates and times.

```java
import java.util.Date;
```

2. **Creating a Date Object**

Next, we need to create a Date object. This can be done by instantiating the Date class.

```java
Date date = new Date();
```

3. **Getting the Unixtime**

Finally, we can get the unixtime by calling the getTime() method on the Date object we just created. This will return the unixtime in milliseconds.

```java
long unixtime = date.getTime();
```

4. **Converting to Seconds**

If we want to convert the unixtime to seconds, we can simply divide the unixtime by 1000.

```java
long unixtimeInSeconds = unixtime / 1000;
```
