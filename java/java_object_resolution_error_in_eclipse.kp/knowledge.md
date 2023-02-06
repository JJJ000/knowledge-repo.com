---
title: When working on a Java project in eclipse, there is an error stating that the type java.lang.object cannot be resolved. this is because it is indirectly referenced from the required .class files
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The Java compiler is unable to find the Object class, which is a part of the Java language, and is required to compile the project.
---

**Contents**

[TOC]

# Solution

## Check Java Version

The most common cause of this error is that you are using a version of Java that is incompatible with the version of Eclipse you are using. To check which version of Java you are using, open the command prompt and type `java -version`. Make sure the version of Java you are using is compatible with the version of Eclipse you are using.

## Check Java Settings

The second possible cause of this error is that the Java settings in Eclipse are not configured correctly. To check your Java settings, open Eclipse and go to `Window > Preferences > Java`. Make sure the correct Java version is selected in the `Installed JREs` section.

## Check Classpath

The third possible cause of this error is that the classpath is not configured correctly. To check your classpath, open Eclipse and go to `Window > Preferences > Java > Build Path > Classpath Variables`. Make sure the `JRE_LIB` variable is set to the correct path for your Java installation.

## Check Project Settings

The fourth possible cause of this error is that the project settings are not configured correctly. To check your project settings, open Eclipse and go to `Project > Properties > Java Build Path`. Make sure the `JRE System Library` is set to the correct version of Java.
