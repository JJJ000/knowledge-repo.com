---
title: Construct a date object with a specified time zone, without using a string representation
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Create a Date object with the Date constructor and pass in the timezone offset in minutes as the second argument.
---

**Contents**

[TOC]

### Creating a Date Object

We can create a Date object in Javascript using the Date constructor. This constructor takes either a single argument, which is a string representation of a date, or multiple arguments that represent the year, month, day, hour, minute, second, and millisecond.

```javascript
const date = new Date(2020, 6, 15, 12, 0, 0);
```

### Setting the Timezone

We can set the timezone of the Date object using the `setTimezoneOffset()` method. This method takes an integer as an argument, representing the offset in minutes from UTC.

```javascript
date.setTimezoneOffset(-300); // -300 minutes from UTC
```

### Checking the Timezone

We can check the timezone of the Date object using the `getTimezoneOffset()` method. This method returns an integer representing the offset in minutes from UTC.

```javascript
date.getTimezoneOffset(); // -300 minutes from UTC
```

### Outputting the Date

We can output the Date object in the desired format using the `toString()` method.

```javascript
date.toString(); // Wed Jul 15 2020 12:00:00 GMT-0500 (Eastern Standard Time)
```
