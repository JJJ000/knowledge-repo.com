---
title: The Android sdk is unable to locate the jdk
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The Android SDK requires a valid JDK to be installed in order to work properly.
---

**Contents**

[TOC]

### Troubleshooting

If the Android SDK installation does not find the JDK in Java, there are a few troubleshooting steps that can be taken. 

### Check the Path

The first step is to check the path of the JDK. The path should be set to the directory where the JDK is installed. If the path is not set correctly, the Android SDK installation will not be able to find the JDK.

### Reinstall the JDK

If the path is set correctly, then it is possible that the JDK is not installed correctly. In this case, it is recommended to uninstall the JDK and reinstall it.

### Check the Environment Variables

Finally, it is possible that the environment variables are not set correctly. To check the environment variables, open the System Properties window and select the Advanced tab. Then select the Environment Variables button. Check that the JAVA_HOME variable is set to the directory of the JDK installation.
