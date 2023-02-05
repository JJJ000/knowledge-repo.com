---
title: The chrome browser cannot be launched due to an error with macos catalina (version 10.15.3) stating that 'chromedriver' cannot be opened because the developer cannot be verified
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To resolve this issue, you need to allow the application to run in System Preferences by selecting `Open Anyway`.
---

**Contents**

[TOC]

## Solution 1: 

1. Open up the System Preferences on your Mac.
2. Select the Security & Privacy option.
3. Select the General tab.
4. Under the "Allow apps downloaded from" section, select the option "Anywhere".
5. Launch the Chrome browser in Java.

## Solution 2: 

1. Open the Terminal on your Mac.
2. Type the command: `sudo spctl --master-disable`
3. Press enter.
4. Launch the Chrome browser in Java.
