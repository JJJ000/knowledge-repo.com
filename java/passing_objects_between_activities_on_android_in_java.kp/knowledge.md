---
title: How to transfer an object between activities on android
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Pass the object by using an Intent`s putExtra() method.
---

**Contents**

[TOC]

### Step 1: Create the Intent

The first step is to create an Intent object, which is a messaging object that can be used to send data between activities.

```java
Intent intent = new Intent(CurrentActivity.this, NextActivity.class);
```

### Step 2: Put the Object into the Intent

Once the Intent is created, the object can be stored in the Intent using the putExtra() method.

```java
intent.putExtra("MyObject", myObject);
```

### Step 3: Start the Activity

To start the new activity, the startActivity() method is called.

```java
startActivity(intent);
```

### Step 4: Retrieve the Object in the New Activity

In the new activity, the object can be retrieved from the Intent using the getSerializableExtra() method.

```java
MyObject myObject = (MyObject) getIntent().getSerializableExtra("MyObject");
```
