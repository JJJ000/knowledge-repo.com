---
title: Error in Android studio "manifest merging failed for apps targeting Android 12."
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The app must be updated to target an Android API level lower than 12.
---

**Contents**

[TOC]

## Overview
Android Studio error "Manifest merger failed: Apps targeting Android 12" occurs when attempting to build an application targeting Android 12. This error occurs when the application's manifest file is incompatible with Android 12.

## Causes
The most common cause of this error is due to the application's manifest file being incompatible with Android 12. This can be due to the application using an older version of the manifest file, or due to the application using an API level that is not supported by Android 12.

## Solutions
The first step to resolving this error is to ensure that the application is targeting the correct API level. The API level should be set to the latest version, which is Android 12.

The second step is to ensure that the application's manifest file is compatible with Android 12. This can be done by updating the manifest file to the latest version, or by removing any incompatible elements from the manifest file.

## Conclusion
The Android Studio error "Manifest merger failed: Apps targeting Android 12" can be resolved by ensuring that the application is targeting the correct API level and that the application's manifest file is compatible with Android 12. By following these steps, the application should be able to be built successfully.
