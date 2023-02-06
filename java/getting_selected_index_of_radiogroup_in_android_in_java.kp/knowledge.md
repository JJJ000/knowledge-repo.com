---
title: What is the method to find the index of the selected item in a radiogroup in android?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the RadioGroup.getCheckedRadioButtonId() method to get the selected index of a RadioGroup in Android.
---

**Contents**

[TOC]

# Section 1: Setup
1. Create a RadioGroup in the XML layout of the Activity.
2. Create a RadioButton for each option in the RadioGroup.

# Section 2: Set an OnCheckedChangeListener
1. In the Activity's onCreate() method, set an OnCheckedChangeListener on the RadioGroup.
2. The OnCheckedChangeListener will have a onCheckedChanged() method that will be called when the selected RadioButton in the RadioGroup is changed.

# Section 3: Retrieve the Selected Index
1. Inside the onCheckedChanged() method, use the getCheckedRadioButtonId() method to get the ID of the selected RadioButton.
2. Use the findViewById() method to get a reference to the RadioGroup.
3. Use the indexOfChild() method to get the index of the selected RadioButton in the RadioGroup.

# Section 4: Store the Selected Index
1. Store the index of the selected RadioButton in a variable or in a SharedPreferences.
2. Use this index to retrieve the selected RadioButton when needed.
