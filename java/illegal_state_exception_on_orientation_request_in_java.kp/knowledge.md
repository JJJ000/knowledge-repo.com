---
title: An activity that is not fullscreen and not opaque cannot request an orientation change and will throw a java.lang.illegalstateexception
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: An activity must be in fullscreen and non-transparent mode in order to request an orientation change.
---

**Contents**

[TOC]

## Symptoms

When attempting to set the orientation of an activity, an IllegalStateException is thrown with the message "Only fullscreen opaque activities can request orientation".

## Cause

This error occurs when an activity is not set to fullscreen and/or not set to be opaque.

## Solution

To resolve this issue, set the activity to fullscreen and opaque. This can be done by adding the following line of code to the onCreate() method of the activity:

`getWindow().addFlags(WindowManager.LayoutParams.FLAG_FULLSCREEN | WindowManager.LayoutParams.FLAG_TRANSLUCENT_STATUS);`

Additionally, the activity must be set to fullscreen in the AndroidManifest.xml file by adding the following line of code:

`android:theme="@android:style/Theme.NoTitleBar.Fullscreen"`
