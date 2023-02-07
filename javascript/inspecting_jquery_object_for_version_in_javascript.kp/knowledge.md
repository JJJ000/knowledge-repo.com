---
title: Find the version of jquery by examining the jquery object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The version of jQuery can be found by inspecting the jQuery object, which is typically `$.fn.jquery`.
---

**Contents**

[TOC]

# Section 1: Retrieve Version from jQuery Object

The version of jQuery can be retrieved from the jQuery object by calling the `jQuery.fn.jquery` method.

# Section 2: Example Code

```javascript
let version = jQuery.fn.jquery;
console.log(version);
```

# Section 3: Output

The output of the code above will be the version of jQuery that is currently being used, for example:

`3.5.1`

# Section 4: Conclusion

By calling the `jQuery.fn.jquery` method, you can easily retrieve the version of jQuery that is currently being used.
