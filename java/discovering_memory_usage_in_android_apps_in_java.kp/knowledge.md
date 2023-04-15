---
title: What is the best way to find out the amount of memory my application is using on an Android device?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the Debug.getMemoryInfo() method to discover memory usage of your application in Android in Java.
---

**Contents**

[TOC]

### Using Android Studio Tools
Android Studio has a set of tools that can be used to measure memory usage of an application. To access these tools, open the Android Monitor window in the Android Studio. This window will show a visual representation of the memory usage of the application. Additionally, the Memory tab in the Android Monitor window will provide details on the memory usage of the application, including the amount of memory allocated and the amount of memory used.

### Using the Android Debug Bridge (ADB)
The Android Debug Bridge (ADB) is a command-line tool that can be used to measure memory usage of an application. To use the ADB, connect the device to the computer and enter the following command:

`adb shell dumpsys meminfo <package name>`

This command will provide detailed information on the memory usage of the application, including the amount of memory allocated and the amount of memory used.

### Using the Android Profiler
The Android Profiler is a tool that can be used to measure memory usage of an application. To use the Android Profiler, open the Android Profiler window in the Android Studio. This window will show a visual representation of the memory usage of the application. Additionally, the Memory tab in the Android Profiler window will provide details on the memory usage of the application, including the amount of memory allocated and the amount of memory used.
