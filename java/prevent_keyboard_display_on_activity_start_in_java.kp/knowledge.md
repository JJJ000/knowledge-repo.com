---
title: Stop the keyboard from appearing when the activity begins
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Call the method `getWindow().setSoftInputMode(WindowManager.LayoutParams.SOFT\_INPUT\_STATE\_HIDDEN);` before `setContentView()` in the `onCreate()` method.
---

**Contents**

[TOC]

### 1. Use the WindowSoftInputMode

The `WindowSoftInputMode` is a setting that allows you to control the behavior of the soft keyboard when the activity is first launched. By setting this to `stateHidden`, the keyboard will not be displayed when the activity is first started.

### 2. Set the Focus of the Window

When the activity is first launched, you can also set the focus of the window to a different view than the one that would normally receive the focus. This can be done by calling the `setFocusable()` method on the view you want to focus on. This will cause the keyboard to not display when the activity is first started.

### 3. Override onCreate()

In the `onCreate()` method of your activity, you can use the `getWindow().setSoftInputMode()` method to set the `stateHidden` flag. This will prevent the keyboard from being displayed when the activity is first launched.

### 4. Use a Custom Keyboard

If you don't want to use the default system keyboard, you can create your own custom keyboard and set it as the default keyboard for your activity. This will prevent the system keyboard from being displayed when the activity is first launched.
