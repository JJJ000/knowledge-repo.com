---
title: What is the best way to convert a JavaScript date object to a JSON string while retaining the timezone?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the Date.prototype.toJSON() method to stringify a Date object and preserve the timezone in the JSON string.
---

**Contents**

[TOC]

### Using toISOString()
The `toISOString()` method returns a string in simplified extended ISO format (ISO 8601), which is always 24 or 27 characters long (YYYY-MM-DDTHH:mm:ss.sssZ or ±YYYYYY-MM-DDTHH:mm:ss.sssZ, respectively).

The following example shows how to use `toISOString()` to JSON stringify a JavaScript Date object and preserve the timezone in the stringified JSON:

```javascript
let date = new Date();
let jsonString = JSON.stringify(date.toISOString());
```

### Using toJSON()
The `toJSON()` method returns a string in the format specified by the toISOString() method, which is always 24 or 27 characters long (YYYY-MM-DDTHH:mm:ss.sssZ or ±YYYYYY-MM-DDTHH:mm:ss.sssZ, respectively).

The following example shows how to use `toJSON()` to JSON stringify a JavaScript Date object and preserve the timezone in the stringified JSON:

```javascript
let date = new Date();
let jsonString = JSON.stringify(date.toJSON());
```

### Using toUTCString()
The `toUTCString()` method returns a string in UTC time (also known as "GMT time" or "Zulu time") in the form of "Day, DD Mon YYYY HH:MM:SS GMT".

The following example shows how to use `toUTCString()` to JSON stringify a JavaScript Date object and preserve the timezone in the stringified JSON:

```javascript
let date = new Date();
let jsonString = JSON.stringify(date.toUTCString());
```

### Using getTimezoneOffset()
The `getTimezoneOffset()` method returns the time-zone offset in minutes for the current locale. The time-zone offset is the difference, in minutes, between UTC and local time.

The following example shows how to use `getTimezoneOffset()` to JSON stringify a JavaScript Date object and preserve the timezone in the stringified JSON:

```javascript
let date = new Date();
let jsonString = JSON.stringify({
  date: date,
  timezoneOffset: date.getTimezoneOffset()
});
```
