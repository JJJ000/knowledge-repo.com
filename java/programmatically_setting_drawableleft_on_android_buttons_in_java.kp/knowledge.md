---
title: What is the best way to assign an image to the left side of an Android button programmatically?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Button.setCompoundDrawablesWithIntrinsicBounds(Drawable left, Drawable top, Drawable right, Drawable bottom);
---

**Contents**

[TOC]

1. **Import the necessary packages**

```java
import android.widget.Button;
import android.graphics.drawable.Drawable;
```

2. **Create a Drawable object**

```java
Drawable drawable = getResources().getDrawable(R.drawable.ic_launcher);
```

3. **Set the drawable on the Button**

```java
Button btn = (Button) findViewById(R.id.button);
btn.setCompoundDrawablesWithIntrinsicBounds(drawable, null, null, null);
```

4. **Set the drawable size**

```java
drawable.setBounds(0, 0, drawable.getMinimumWidth(), drawable.getMinimumHeight());
```
