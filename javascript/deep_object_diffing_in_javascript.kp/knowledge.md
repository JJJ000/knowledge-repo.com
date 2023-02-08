---
title: A comparison of the differences between two objects using a deep comparison algorithm
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: A deep diff between two objects in Javascript is the process of comparing two objects and finding all the differences between them, including differences in their nested objects and arrays.
---

**Contents**

[TOC]

### Section 1: Shallow Diff
Shallow diff compares two objects to determine the differences between their properties. It looks only at the top level of the objects and does not compare nested objects. To perform a shallow diff, the two objects are compared to each other and the differences between their properties are identified.

### Section 2: Deep Diff
Deep diff is a more comprehensive comparison between two objects. It looks at the nested objects within each object and compares them to determine the differences between them. To perform a deep diff, the two objects are recursively compared to each other and the differences between their properties and nested objects are identified.

### Section 3: Implementation
The implementation of a deep diff can be done using a recursive approach. The two objects are compared and if the properties are the same, the comparison is complete. If the properties are different, the nested objects of each object are compared and the differences are identified. This process is repeated until all the differences between the two objects have been identified.

### Section 4: Benefits
Deep diff provides a comprehensive comparison between two objects and can be used to identify any differences between them. It is a useful tool for debugging and understanding the differences between two objects. It can also be used to identify any changes that have been made to an object over time.
