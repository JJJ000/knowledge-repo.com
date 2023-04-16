---
title: What is the syntax for setting a JavaScript date object to a specific time zone?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can initialize a JavaScript Date to a particular time zone by using the Date.UTC() method.
---

**Contents**

[TOC]

# Section 1: Importing Time Zone Library

In order to set a Date object to a specific time zone, you will need to import a time zone library. The most popular library for this purpose is the [Moment Timezone library](https://momentjs.com/timezone/).

# Section 2: Setting a Date Object

Once you have imported the Moment Timezone library, you can create a Date object and set it to a particular time zone. To do this, you can use the `tz` method of the Moment Timezone library. This method takes two parameters: the date you want to set and the time zone you want to set it to.

For example, to set a date object to the Eastern Standard Time (EST) time zone, you could use the following code:

```javascript
const date = moment.tz(new Date(), 'America/New_York');
```

# Section 3: Displaying Date in a Specific Time Zone

Once you have set the Date object to a particular time zone, you can display it in that time zone. To do this, you can use the `format` method of the Moment Timezone library. This method takes two parameters: the format you want to display the date in and the time zone you want to display it in.

For example, to display the date in the Eastern Standard Time (EST) time zone, you could use the following code:

```javascript
const dateString = date.format('DD/MM/YYYY hh:mm:ss A z', 'America/New_York');
```

# Section 4: Converting Date to a Specific Time Zone

Finally, you can also convert a Date object from one time zone to another. To do this, you can use the `tz` method of the Moment Timezone library. This method takes two parameters: the date you want to convert and the time zone you want to convert it to.

For example, to convert the date from the Eastern Standard Time (EST) time zone to the Pacific Standard Time (PST) time zone, you could use the following code:

```javascript
const date = moment.tz(date, 'America/Los_Angeles');
```
