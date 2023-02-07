---
title: What is the output of console.log timestamps in chrome?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: In Chrome, JavaScript console logs can be timestamped by using the `console.time()` and `console.timeEnd()` methods.
---

**Contents**

[TOC]

# Using Date.now()

The easiest way to log a timestamp in Chrome using Javascript is to use the `Date.now()` method. This method returns the number of milliseconds elapsed since January 1, 1970 00:00:00 UTC.

Example:

```
console.log(Date.now());
```

# Using Date Constructor

You can also use the `Date` constructor to log a timestamp in Chrome using Javascript. The `Date` constructor takes a single parameter, the number of milliseconds elapsed since January 1, 1970 00:00:00 UTC, and returns a Date object representing that date and time.

Example:

```
console.log(new Date(Date.now()));
```

# Using toISOString()

If you want to log a timestamp in a more readable format, you can use the `toISOString()` method. This method returns a string in the ISO 8601 format, which is a standardized format for representing dates and times.

Example:

```
console.log(new Date(Date.now()).toISOString());
```

# Using toLocaleString()

Finally, you can use the `toLocaleString()` method to log a timestamp in the local timezone. This method takes two parameters, a locale string and an options object, and returns a string representing the date and time in the specified locale.

Example:

```
console.log(new Date(Date.now()).toLocaleString('en-US', { timeZone: 'America/Los_Angeles' }));
```
