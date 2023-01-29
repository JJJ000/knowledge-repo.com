---
title: How can I start an activity from another application in android?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use an Intent object with the Context.startActivity() method to launch an Activity from another Application in Android.
---

**Contents**

[TOC]

### Step 1: Create an Intent

The first step to launching an Activity from another application is to create an Intent. An Intent is an object that provides runtime binding between separate components such as two activities. The Intent can be used to start an Activity, send a broadcast, or deliver a message.

### Step 2: Set the Intent's Action

The next step is to set the Intent's action. This is used to specify the type of action to be performed. There are several actions available such as ACTION_VIEW, ACTION_EDIT, ACTION_SEND, etc.

### Step 3: Set the Intent's Data

The Intent's data is used to provide the target application with the data it needs to perform the action. This can be a Uri, a file, or any other type of data.

### Step 4: Start the Activity

The last step is to start the Activity. This is done by calling the startActivity() method with the Intent as a parameter. This will start the Activity in the target application with the data provided in the Intent.
