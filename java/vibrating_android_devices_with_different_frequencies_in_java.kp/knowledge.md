---
title: What is the process for producing varying levels of vibration on an Android device?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Vibrator class` vibrate() method, passing in a desired frequency in milliseconds.
---

**Contents**

[TOC]

### Using Vibration

Android provides access to the device's vibration hardware through the Vibrator class. To make an Android device vibrate, you need to get an instance of the Vibrator class:

```java
Vibrator vibrator = (Vibrator) getSystemService(Context.VIBRATOR_SERVICE);
```

### Vibrate with a Pattern

To make an Android device vibrate with a pattern, you can use the `vibrate(long[] pattern, int repeat)` method. The `pattern` parameter is an array of longs of times for which to turn the vibrator on or off. The `repeat` parameter is the index into the pattern array at which to start repeating. The following code example makes an Android device vibrate with a pattern of 500ms on, 500ms off, 500ms on, 1s off, 500ms on, and repeats this pattern twice:

```java
vibrator.vibrate(new long[]{500, 500, 500, 1000, 500}, 2);
```

### Vibrate with a Frequency

To make an Android device vibrate with a frequency, you can use the `vibrate(long milliseconds)` method. This method takes a single long parameter which is the number of milliseconds to vibrate for. For example, the following code makes an Android device vibrate for 500 milliseconds:

```java
vibrator.vibrate(500);
```

### Stop Vibrating

To stop an Android device from vibrating, you can use the `cancel()` method. This method stops the device from vibrating immediately. The following code stops an Android device from vibrating:

```java
vibrator.cancel();
```
