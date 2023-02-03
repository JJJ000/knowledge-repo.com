---
title: Retrieving the identifier of the element that triggered an event
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The ID of the element that fired an event can be obtained using the event`s `target` property.
---

**Contents**

[TOC]

**Section 1: Accessing the Event Target**

The ID of the element that fired an event can be accessed by using the `event.target` property. This property returns the element that triggered the event. 

**Section 2: Accessing the ID of the Event Target**

Once the event target has been accessed, the ID of the element can be accessed by using the `event.target.id` property. This will return the ID of the element that triggered the event. 

**Section 3: Using the ID**

Once the ID of the element that triggered the event has been accessed, it can be used in any way desired. For example, it could be used to access the element in the DOM or to access data associated with the element. 

**Section 4: Example Code**

Here is an example of how to access the ID of the element that fired an event:

```javascript
document.addEventListener("click", (event) => {
  let id = event.target.id;
  console.log(id);
});
```
