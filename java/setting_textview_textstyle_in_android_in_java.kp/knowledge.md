---
title: How to change the font style of a textview in Android through code?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: TextViews can be styled programmatically in Java using the setTypeface() method.
---

**Contents**

[TOC]

`**` Declaring TextView**

To set TextView TextStyle programmatically in Java, first declare a TextView in the Activity class.

```java
TextView textView = findViewById(R.id.textView);
```

`**` Setting TextStyle**

Next, set the TextStyle of the TextView by using the setTypeface() method.

```java
textView.setTypeface(Typeface.create("serif", Typeface.ITALIC));
```

`**` Setting TextSize**

To set the TextSize of the TextView, use the setTextSize() method.

```java
textView.setTextSize(TypedValue.COMPLEX_UNIT_SP, 20);
```

`**` Setting Text Color**

Finally, to set the Text Color of the TextView, use the setTextColor() method.

```java
textView.setTextColor(Color.parseColor("#000000"));
```
