---
title: Change the functionality of the back button to mimic the home button
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Override the onBackPressed() method to call the finish() method.
---

**Contents**

[TOC]

# Solution

## Step 1: Override the onBackPressed() Method

The first step to overriding the back button to act like a home button is to override the `onBackPressed()` method. This method is called when the back button is pressed.

```java
@Override 
public void onBackPressed() { 
  // code to be executed when back button is pressed 
} 
```

## Step 2: Create an Intent

The next step is to create an intent to launch the home screen activity.

```java
Intent intent = new Intent(Intent.ACTION_MAIN); 
intent.addCategory(Intent.CATEGORY_HOME); 
intent.setFlags(Intent.FLAG_ACTIVITY_NEW_TASK); 
startActivity(intent); 
```

## Step 3: Finish the Activity

The last step is to finish the current activity.

```java
finish(); 
```

## Step 4: Put It All Together

Putting it all together, the `onBackPressed()` method should look like this:

```java
@Override 
public void onBackPressed() { 
  Intent intent = new Intent(Intent.ACTION_MAIN); 
  intent.addCategory(Intent.CATEGORY_HOME); 
  intent.setFlags(Intent.FLAG_ACTIVITY_NEW_TASK); 
  startActivity(intent); 
  finish(); 
} 
```
