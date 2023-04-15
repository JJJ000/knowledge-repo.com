---
title: What is the method to obtain the number of seconds since epoch using the time and date output of gmtime()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the `time.mktime()` function with the output of `gmtime()` to get the seconds since epoch.
---

**Contents**

[TOC]

# Converting time + date output of gmtime() to seconds since epoch in Python

## Introduction
In Python, the `gmtime()` function from the `time` module returns the Coordinated Universal Time (UTC) as a struct time object which includes information about the date and time. However, sometimes we need to convert this information into seconds since the Unix epoch, which is the number of seconds that have elapsed since January 1, 1970, at 00:00:00 UTC. In this tutorial, we will discuss how to get the seconds since epoch from the time + date output of gmtime() in Python.

## Step 1: Importing the time module
The first step is to import the `time` module in our Python script. We can do this by using the following code:

``` python
import time
```

## Step 2: Getting the struct time object from gmtime()
The next step is to get the struct time object from the `gmtime()` function. We can do this by calling `gmtime()` without any arguments. For example:

``` python
import time

t = time.gmtime()
```

## Step 3: Converting the struct time object to seconds since epoch
Now that we have the struct time object, we can convert it into seconds since epoch. We can use the `mktime()` function from the `time` module to do this. The `mktime()` function takes a struct time object as an argument and returns the corresponding number of seconds since epoch. For example:

``` python
import time

t = time.gmtime()
seconds_since_epoch = time.mktime(t)
```

## Step 4: Printing the seconds since epoch
Finally, we can print the number of seconds since epoch to the console. For example:

``` python
import time

t = time.gmtime()
seconds_since_epoch = time.mktime(t)
print("Seconds since epoch:", seconds_since_epoch)
```

This will output something like:

```
Seconds since epoch: 1621584839.0
```

Note that `mktime()` returns the number of seconds as a floating-point value, so we get the ".0" at the end. We can use the `int()` function to convert this to an integer if we don't need the decimal part.
