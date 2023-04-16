---
title: What is the distinction between onintercepttouchevent and dispatchtouchevent in android?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: onInterceptTouchEvent is used to intercept a touch event before it is passed to the child view, while dispatchTouchEvent is used to dispatch a touch event to the view`s onTouchEvent method.
---

**Contents**

[TOC]

# onInterceptTouchEvent

onInterceptTouchEvent is a method of the ViewGroup class. It is called whenever a touch event is detected on the ViewGroup, before the child views receive the event. Its purpose is to decide whether the ViewGroup should intercept the touch event and handle it itself, or if it should pass the event to its child views.

# dispatchTouchEvent

dispatchTouchEvent is a method of the View class. It is called whenever a touch event is detected on the View. Its purpose is to dispatch the touch event to the appropriate child views. It is responsible for deciding which view should receive the touch event, and for calling the appropriate onTouchEvent method on the view.

# Difference

The main difference between onInterceptTouchEvent and dispatchTouchEvent is that onInterceptTouchEvent is called on the ViewGroup, while dispatchTouchEvent is called on the View. Additionally, onInterceptTouchEvent is called before the child views receive the event, while dispatchTouchEvent is called after the event has been received by the View.
