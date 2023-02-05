---
title: Programmatically closing a jframe can be done by calling the dispose() method on the frame
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The JFrame can be closed programmatically by calling the dispose() method.
---

**Contents**

[TOC]

# Option 1: Using dispose()

The `dispose()` method of the `JFrame` class can be used to programmatically close a `JFrame`. This method will close the `JFrame` and release all of its resources.

# Option 2: Using setVisible(false)

The `setVisible(false)` method of the `JFrame` class can also be used to programmatically close a `JFrame`. This method will hide the `JFrame` but not release its resources.

# Option 3: Using System.exit(0)

The `System.exit(0)` method can be used to programmatically close a `JFrame`. This method will exit the program and close all `JFrame`s.

# Option 4: Using WindowListener

The `WindowListener` interface can be used to programmatically close a `JFrame`. This interface allows you to add a listener to the `JFrame` that will be triggered when the `JFrame` is closed.
