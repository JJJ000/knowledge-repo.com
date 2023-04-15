---
title: What is the best way to create a delay in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the Thread.sleep() method to create a delay in Java.
---

**Contents**

[TOC]

### Using Thread.sleep()
Thread.sleep() is a static method of the Thread class that can be used to pause the execution of the program for a given amount of time. 

Syntax:
```
Thread.sleep(milliseconds)
```

Example:
```
Thread.sleep(5000); // pauses the execution for 5 seconds
```

### Using Timer and TimerTask
The Timer and TimerTask classes provide a means for executing code after a specified amount of time.

Example:
```
Timer timer = new Timer();
timer.schedule(new TimerTask() {
    @Override
    public void run() {
        // code to be executed
    }
}, 5000); // executes the code after 5 seconds
```
