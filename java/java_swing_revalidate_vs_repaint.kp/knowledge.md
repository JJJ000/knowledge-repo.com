---
title: What are the differences between the Java swing revalidate() and repaint() methods?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The revalidate() method is used to indicate that a container`s layout needs to be recomputed, while the repaint() method is used to update the container`s display.
---

**Contents**

[TOC]

## revalidate()
`revalidate()` is a method used to indicate that if the layout of a component has been changed, it needs to be revalidated. This method will cause the layout manager to recalculate the layout of the component and its subcomponents.

## repaint()
`repaint()` is a method used to indicate that a component needs to be repainted. This method will cause the component to be redrawn with its current state.

## Difference
The main difference between `revalidate()` and `repaint()` is that `revalidate()` is used to indicate that the layout of a component has changed and needs to be recalculated, while `repaint()` is used to indicate that the component needs to be redrawn with its current state.
