---
title: Identify a finger swipe using JavaScript on both the iphone and android
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: It is not possible to detect a finger swipe through JavaScript on the iPhone and Android.
---

**Contents**

[TOC]

1. Detecting Swipe on iOS
--------------------------------

Detecting a finger swipe on an iOS device can be done using the `touches` event. This event will fire when a user touches the screen, and can be used to detect a swipe motion. The `touches` event will also provide the x and y coordinates of the user's finger, allowing us to track the direction and speed of the swipe.

2. Detecting Swipe on Android
--------------------------------

Detecting a finger swipe on an Android device can be done using the `touchstart` and `touchend` events. This event will fire when a user touches the screen, and can be used to detect a swipe motion. The `touchstart` and `touchend` events will also provide the x and y coordinates of the user's finger, allowing us to track the direction and speed of the swipe.

3. Using JavaScript to Detect Swipe
-----------------------------------

To detect a finger swipe using JavaScript, we can use the `touches` event on iOS devices, and the `touchstart` and `touchend` events on Android devices. We can then use the x and y coordinates of the user's finger to detect the direction and speed of the swipe.

4. Conclusion
----------------

Detecting a finger swipe on an iOS or Android device can be done using the `touches` event on iOS devices, and the `touchstart` and `touchend` events on Android devices. Using the x and y coordinates of the user's finger, we can track the direction and speed of the swipe motion.
