---
title: Testing if an input has focus using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: $(selector).is(`focus`) can be used to test if an input has focus in Javascript.
---

**Contents**

[TOC]

####Using the .is() Method

The .is() method can be used to test if an input has focus in jQuery. This method checks if the selected element matches the selector.

```
if($("input").is(":focus")) {
  //Do something
}
```

####Using the .focus() Method

The .focus() method can also be used to test if an input has focus in jQuery. This method sets focus on the specified element.

```
if($("input").focus()) {
  //Do something
}
```

####Using the .hasClass() Method

The .hasClass() method can be used to test if an input has focus in jQuery. This method checks if the selected element has the specified class.

```
if($("input").hasClass("focus")) {
  //Do something
}
```

####Using the .is() Method

The .is() method can also be used to test if an input has focus in jQuery. This method checks if the selected element is the specified selector.

```
if($("input").is(":focus")) {
  //Do something
}
```
