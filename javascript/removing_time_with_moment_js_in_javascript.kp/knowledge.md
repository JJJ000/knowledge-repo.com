---
title: What is the best way to subtract time from a date using moment.js?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the `moment().startOf(`day`)` method to remove time from a date with Moment.js.
---

**Contents**

[TOC]

### Using Moment.js

Moment.js provides a `startOf()` method that allows you to set the time of a given Moment object to the start of a unit of time. This can be used to remove the time from a date.

### Syntax

The syntax for the `startOf()` method is `moment().startOf(unitOfTime)`, where `unitOfTime` is the unit of time that you want to set the Moment object to the start of. This can be any of the following units:

- `year`
- `month`
- `week`
- `day`
- `hour`
- `minute`
- `second`
- `millisecond`

### Example

For example, if you have a Moment object representing the date `2020-05-19T10:15:30`, you can remove the time by using the `startOf()` method like this:

```javascript
const date = moment('2020-05-19T10:15:30');
date.startOf('day');
// Output: Moment("2020-05-19T00:00:00")
```

### Output

The output of the `startOf()` method is a new Moment object with the time set to the start of the specified unit of time. In the example above, the output is `Moment("2020-05-19T00:00:00")`, which is the same date with the time set to `00:00:00`.
