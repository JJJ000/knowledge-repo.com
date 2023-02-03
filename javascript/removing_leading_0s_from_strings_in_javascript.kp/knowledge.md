---
title: Remove the 0 at the beginning of the string if it is present
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the substring() method to remove the first character of a string if it is 0.
---

**Contents**

[TOC]

##### Section 1 

Check if the First Character is 0

##### Section 2

Create a Substring

##### Section 3

Replace the String

##### Section 4

Return the Result

Code:

```
let str = "0123456789";

if (str.charAt(0) === '0') {
  let substr = str.substring(1);
  str = str.replace(str, substr);
}

return str;
```

Result: "123456789"
