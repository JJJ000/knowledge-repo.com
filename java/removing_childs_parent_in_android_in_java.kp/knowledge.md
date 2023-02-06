---
title: You must first call removeview() on the parent of the specified child before you can continue, as the child already has a parent
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You must call removeView() on the child`s parent before adding it to a new parent.
---

**Contents**

[TOC]

**1. Get Parent View:** 

```java
ViewGroup parentView = (ViewGroup) childView.getParent();
```

**2. Remove Child View:**

```java
parentView.removeView(childView);
```

**3. Add Child View to New Parent:**

```java
newParentView.addView(childView);
```

**4. Request Layout:**

```java
newParentView.requestLayout();
```
