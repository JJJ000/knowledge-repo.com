---
title: Which jdk should I use for netbeans?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Set the `netbeans\_jdkhome` environment variable to the path of the desired JDK.
---

**Contents**

[TOC]

## Set Environment Variables

1. Open the System Properties window by right-clicking on "This PC" and selecting "Properties".

2. Select the "Advanced System Settings" option on the left side of the window.

3. Click the "Environment Variables" button at the bottom of the window.

4. Under the "System Variables" section, click the "New" button.

5. Enter "JAVA_HOME" as the Variable name and the path to the JDK installation as the Variable value.

6. Click "OK" to save the changes.

## Configure NetBeans

1. Open NetBeans and navigate to "Tools" > "Options" > "Java".

2. Under the "Platform Settings" tab, select the "Add Platform" button.

3. Select the "Java Home" option and click the "Browse" button.

4. Select the folder of the JDK installation and click "OK".

5. Click the "OK" button to save the changes and close the window.
