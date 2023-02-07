---
title: Look for modifications in the dom
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The DOM can be monitored for changes using the MutationObserver API.
---

**Contents**

[TOC]

**1. Using the DOM Mutation Events**

The DOM Mutation Events are events that are fired when the DOM is changed. These events can be used to detect changes in the DOM by listening for the events.

**2. Using the MutationObserver**

The MutationObserver is an object that can be used to detect changes in the DOM. It allows you to specify what type of changes you are looking for and will fire a callback when the changes occur.

**3. Using the getElementsByTagName() Method**

The getElementsByTagName() method can be used to detect changes in the DOM. This method will return a list of elements with the specified tag name. You can then compare the list of elements before and after the change in the DOM to detect the changes.

**4. Using the setInterval() Method**

The setInterval() method can be used to periodically check the DOM for changes. This method will execute a callback at the specified interval and can be used to compare the DOM before and after the interval to detect any changes.
