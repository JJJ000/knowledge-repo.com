---
title: Altering the bottom line color of an edittext using appcompat v7
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the setBackgroundTintList() method on the EditText object to change the bottom line color.
---

**Contents**

[TOC]

`**` Setting up the AppCompat v7 Library**

1. Open the Android Studio project and select File > Project Structure.
2. Select the Dependencies tab and click the + button.
3. Select Library Dependency and search for appcompat-v7.
4. Select the appropriate version from the list and click OK.

`**` Adding the Color Resource**

1. Open the res/values/colors.xml file and add a new color resource for the bottom line of the EditText.
2. Set the color hex code to the desired color.

`**` Setting the Color on the EditText**

1. Open the layout file containing the EditText and add the following attribute to the EditText:
```
android:backgroundTint="@color/<color_resource_name>"
```

`**` Setting the Color Programmatically**

1. Get a reference to the EditText in the Activity or Fragment.
2. Use the following code to set the color programmatically:
```
editText.getBackground().setColorFilter(ContextCompat.getColor(this, R.color.<color_resource_name>), PorterDuff.Mode.SRC_IN);
```
