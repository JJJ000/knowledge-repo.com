---
title: Install Android development tools version 23 in eclipse
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To update Eclipse with Android development tools v. 23 in Java, you need to install the Android SDK and ADT Plugin for Eclipse.
---

**Contents**

[TOC]

### Step 1: Download Android Studio

1. Download Android Studio from the [Android Developer website](https://developer.android.com/studio).

2. Follow the on-screen instructions to install Android Studio.

### Step 2: Configure Android Studio

1. Launch Android Studio and select "Configure" > "SDK Manager".

2. In the SDK Manager window, select the "SDK Platforms" tab and check the box next to "Android SDK Platform 23".

3. Select the "SDK Tools" tab and check the box next to "Android SDK Build-Tools 23".

4. Click "Apply" and wait for the components to download and install.

### Step 3: Configure Eclipse

1. Launch Eclipse and select "Window" > "Preferences".

2. In the left panel, select "Android" and enter the path to the Android SDK in the "SDK Location" field.

3. Click "Apply" and then "OK" to save the changes.

### Step 4: Install ADT Plugin

1. In Eclipse, select "Help" > "Install New Software".

2. In the "Work with" field, enter the following URL: https://dl-ssl.google.com/android/eclipse/.

3. Check the box next to "Developer Tools" and click "Next".

4. Read and accept the license agreement, then click "Finish".

5. Restart Eclipse when prompted.
