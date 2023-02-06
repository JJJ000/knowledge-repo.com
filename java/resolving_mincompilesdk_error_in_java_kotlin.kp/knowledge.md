---
title: What is the best way to fix the problem of the "mincompilesdk (31) specified in a dependency's aar metadata" error when using native Java or kotlin?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Update the compileSdkVersion in the app`s build.gradle file to the same version as the minCompileSdk specified in the AAR metadata.
---

**Contents**

[TOC]

## Step 1: Check the SDK Version

Check the SDK version of the dependency and make sure it matches the minCompileSdk version specified in the project.

## Step 2: Update the SDK Version

If the SDK version of the dependency does not match the minCompileSdk version specified in the project, update the SDK version of the dependency to match the minCompileSdk version specified in the project.

## Step 3: Clean the Project

Once the SDK version of the dependency has been updated, clean the project to ensure the changes are applied.

## Step 4: Rebuild the Project

Rebuild the project after cleaning it to ensure the changes are applied.
