---
title: What is the syntax for using jq to filter a JSON that does not have a certain value?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: Use the `not` operator with the `contains` filter to select JSON elements that do not contain a certain value.
---

**Contents**

[TOC]

### Section 1: Using the .not() Method
The .not() method can be used to filter a JSON object that does not contain a specific value. The syntax for the .not() method is: 

```
$(selector).not(filter)
```

Where `selector` is a selector expression to match elements against and `filter` is a selector expression to filter matching elements.

### Section 2: Example
For example, to filter a JSON object that does not contain the value `"foo"`, the following code can be used: 

```
$.each(json, function(key, value) {
    if (value != "foo") {
        // Do something with the non-foo value
    }
});
```

### Section 3: Using the .filter() Method
The .filter() method can also be used to filter a JSON object that does not contain a specific value. The syntax for the .filter() method is: 

```
$(selector).filter(callback[, thisObject])
```

Where `selector` is a selector expression to match elements against, `callback` is a function to test each element of the array, and `thisObject` is an optional object to use as `this` when executing the callback.

### Section 4: Example
For example, to filter a JSON object that does not contain the value `"foo"`, the following code can be used: 

```
var filteredJSON = $(json).filter(function(i,v) {
    return v != "foo";
});
```
