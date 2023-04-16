---
title: How can I set a JavaScript date to midnight?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The best way to initialize a JavaScript Date to midnight is to create a Date object with the arguments of the year, month, and day set to the desired date.
---

**Contents**

[TOC]

### Using Constructor

The Date constructor can be used to initialize a Date object to midnight by passing in the year, month, and day parameters. 

```
var midnight = new Date(year, month, day);
```

### Using Setters

The Date.setFullYear(), Date.setMonth(), and Date.setDate() methods can be used to set the year, month, and day of a Date object respectively. 

```
var midnight = new Date();
midnight.setFullYear(year);
midnight.setMonth(month);
midnight.setDate(day);
```

### Using UTC

The Date.UTC() method can be used to create a Date object set to midnight in UTC time. 

```
var midnight = new Date(Date.UTC(year, month, day));
```

### Using Timestamp

The Date.now() method can be used to get the current timestamp and the Date constructor can be used to create a Date object from the timestamp. 

```
// Get the current timestamp
var timestamp = Date.now();

// Get the midnight timestamp
var midnightTimestamp = new Date(year, month, day).getTime();

// Create the Date object from the midnight timestamp
var midnight = new Date(midnightTimestamp);
```
