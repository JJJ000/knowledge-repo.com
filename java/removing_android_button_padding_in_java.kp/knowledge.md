---
title: What is the best way to get rid of the space around buttons in an Android application?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the setPadding(0, 0, 0, 0) method on the Button object.
---

**Contents**

[TOC]

# Section 1: Finding the Layout File
The first step to removing padding around buttons in Android is to locate the layout file. This file is typically located in the res/layout folder of the Android project.

# Section 2: Editing the Layout File
Once the layout file is located, the next step is to edit the layout file. This is done by opening the file in a text editor and adding the following line of code:

android:padding="0dp"

# Section 3: Testing the Changes
After the code is added to the layout file, the changes can be tested by running the application. If the changes are successful, the padding around the buttons should be removed.

# Section 4: Saving the Changes
Once the changes have been tested, the layout file should be saved and the application should be re-run to ensure the changes are saved.
