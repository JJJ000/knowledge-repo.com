---
title: What is the difference in days between two dates?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the Date.now() method to calculate the difference between two dates in milliseconds, then divide the result by the number of milliseconds in a day (86400000) to get the number of days between the two dates.
---

**Contents**

[TOC]

# Section 1: Using Date Object

The Date object in JavaScript allows us to create Date instances and manipulate them. To calculate the number of days between two dates, we can use the getTime() method to get the number of milliseconds since January 1, 1970, and then subtract the two dates.

# Section 2: Creating Date Objects

To create Date objects, we can use the Date constructor, which takes a number of arguments. For example, the following code creates a Date object for April 1, 2021:

```
var date1 = new Date(2021, 3, 1);
```

The arguments for the Date constructor are the year, month (0-11), and day (1-31).

# Section 3: Calculating the Difference

Once we have two Date objects, we can calculate the difference between them in days by subtracting the two dates and dividing by the number of milliseconds in a day (1000 * 60 * 60 * 24). The following code calculates the difference between two dates in days:

```
var dateDiff = (date2.getTime() - date1.getTime()) / (1000 * 60 * 60 * 24);
```

# Section 4: Example

To demonstrate, let's calculate the number of days between April 1, 2021 and April 15, 2021. First, we create two Date objects:

```
var date1 = new Date(2021, 3, 1);
var date2 = new Date(2021, 3, 15);
```

Then, we can calculate the difference:

```
var dateDiff = (date2.getTime() - date1.getTime()) / (1000 * 60 * 60 * 24);

// dateDiff = 14
```

The result is 14 days.
