---
title: What makes react's virtual dom said to be more efficient than traditional dirty model checking?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: React`s Virtual DOM is more performant than dirty model checking in Javascript because it only re-renders the components that have changed, rather than the entire DOM, which saves time and resources.
---

**Contents**

[TOC]

1. What is Dirty Model Checking?

Dirty model checking is a technique used in Javascript to detect changes in the DOM tree. It works by comparing the current DOM tree with a stored version of the DOM tree. If there are any differences between the two, the code is executed to update the DOM tree accordingly.

2. What is Virtual DOM?

Virtual DOM is a concept used in React to create an in-memory representation of the DOM tree. This representation is then used to compare with the actual DOM tree and to update the DOM tree accordingly.

3. Advantages of Virtual DOM

Virtual DOM is more performant than dirty model checking because it does not need to compare the entire DOM tree every time. Instead, it only compares the parts of the DOM tree that have changed. This makes the process of updating the DOM tree much faster and more efficient.

4. Conclusion

In conclusion, React's concept of Virtual DOM is more performant than dirty model checking in Javascript because it only compares the parts of the DOM tree that have changed instead of the entire DOM tree. This makes the process of updating the DOM tree much faster and more efficient.
