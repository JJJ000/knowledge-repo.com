---
title: Pressing the back button twice to end an activity
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To exit an activity in Java, press the back button twice.
---

**Contents**

[TOC]

### Using onBackPressed()

The `onBackPressed()` method can be used to exit an activity when the back button is pressed. This method is called when the back button is pressed and it can be used to perform an action such as exiting the activity. To exit an activity when the back button is pressed twice, the `onBackPressed()` method can be used to check if the back button has been pressed twice and then perform the action.

### Using a Boolean Variable

A boolean variable can also be used to check if the back button has been pressed twice. This variable can be set to true when the back button is pressed the first time and then set to false when the back button is pressed the second time. If the variable is true when the back button is pressed the second time, then the action to exit the activity can be performed.

### Using a Timer

A timer can also be used to check if the back button has been pressed twice. The timer can be set to a certain amount of time and when the back button is pressed the timer will start. If the back button is pressed again before the timer has finished, then the action to exit the activity can be performed.

### Using a Counter

A counter can also be used to check if the back button has been pressed twice. The counter can be set to 0 when the activity starts and then incremented when the back button is pressed. If the counter is 2 when the back button is pressed, then the action to exit the activity can be performed.
