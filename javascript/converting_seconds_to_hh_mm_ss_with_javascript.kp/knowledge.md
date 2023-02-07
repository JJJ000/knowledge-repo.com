---
title: How can I use JavaScript to change seconds into hours, minutes and seconds?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can convert seconds to HH-MM-SS with JavaScript by using the Date object and its methods getHours(), getMinutes(), and getSeconds().
---

**Contents**

[TOC]

#### Section 1: Create a Function

We will create a function to convert seconds to HH-MM-SS.

```javascript
function secondsToHMS(seconds) {
  let h = Math.floor(seconds / 3600);
  let m = Math.floor(seconds % 3600 / 60);
  let s = Math.floor(seconds % 3600 % 60);

  return ((h > 0 ? h + ":" + (m < 10 ? "0" : "") : "") + m + ":" + (s < 10 ? "0" : "") + s);
}
```

#### Section 2: Usage

We can use the function like this:

```javascript
let seconds = 3600;
let hms = secondsToHMS(seconds); // 1:00:00
```

#### Section 3: Test Cases

We can test the function with a few test cases:

```javascript
console.log(secondsToHMS(3600)); // 1:00:00
console.log(secondsToHMS(3601)); // 1:00:01
console.log(secondsToHMS(3660)); // 1:01:00
console.log(secondsToHMS(3661)); // 1:01:01
```

#### Section 4: Output

The output of the test cases should be:

```
1:00:00
1:00:01
1:01:00
1:01:01
```
