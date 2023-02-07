---
title: Scroll the overflow div to the bottom unless the user manually scrolls it up
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the scrollTop property to set the scroll position to the bottom of the div when the user scrolls down, and check the scroll position to prevent it from resetting to the bottom when the user scrolls up.
---

**Contents**

[TOC]

**Section 1: Add a Scroll Event Listener**

We need to add an event listener to the overflow div so that we can detect when the user scrolls up. We can use the `addEventListener` method to do this:

```javascript
overflowDiv.addEventListener('scroll', function(e) {
  // scroll event handler code goes here
});
```

**Section 2: Store the Initial Scroll Position**

We need to store the initial scroll position of the overflow div so that we can compare it to the current scroll position later. We can use the `scrollTop` property to get the initial scroll position:

```javascript
let initialScrollPosition = overflowDiv.scrollTop;
```

**Section 3: Check the Scroll Position**

We need to check the scroll position of the overflow div every time the user scrolls. We can do this by checking the `scrollTop` property of the overflow div in the event handler:

```javascript
let currentScrollPosition = overflowDiv.scrollTop;
```

**Section 4: Scroll to Bottom if Necessary**

Now that we have the initial and current scroll positions, we can compare them to determine if the user has scrolled up. If they have, we can do nothing. If they have not, we can scroll the overflow div to the bottom:

```javascript
if (currentScrollPosition === initialScrollPosition) {
  overflowDiv.scrollTop = overflowDiv.scrollHeight;
}
```
