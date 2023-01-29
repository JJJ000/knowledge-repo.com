---
title: How can I programmatically set a background drawable in android?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: View.setBackgroundDrawable(Drawable drawable) can be used to set a Drawable as the background of a View in Android programmatically in Java.
---

**Contents**

[TOC]

### Step 1: Create a Drawable

Create a drawable resource in `res/drawable` directory of your project. For example, `my_background.xml`.

### Step 2: Reference the Drawable

Reference the drawable in the layout file of your activity. For example,

```xml
<RelativeLayout
    android:id="@+id/layout"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@drawable/my_background" />
```

### Step 3: Set the Drawable Programmatically

In the activity class, set the background drawable programmatically. For example,

```java
RelativeLayout layout = findViewById(R.id.layout);
layout.setBackground(getDrawable(R.drawable.my_background));
```
