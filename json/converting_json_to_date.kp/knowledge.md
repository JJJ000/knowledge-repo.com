---
title: Transforming JSON outcomes into a date
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can use the JavaScript Date constructor to convert JSON results to a date.
---

**Contents**

[TOC]

##### Creating a Date Object from JSON

In order to convert a JSON result to a date, you will need to first create a `Date` object from the JSON result. This can be done by passing the JSON result to the `Date` constructor, as shown below:

```javascript
let jsonResult = {
  "year": 2020,
  "month": 4,
  "day": 20
};

let date = new Date(jsonResult.year, jsonResult.month - 1, jsonResult.day);
```

In the above example, we are creating a `Date` object by passing in the year, month, and day values from the JSON result. Note that the month value is subtracted by one as the `Date` constructor expects the month value to be zero-based.

##### Formatting the Date

Once the `Date` object has been created, you can use the `toLocaleDateString()` method to format the date as desired. This method takes two arguments - the locale and the options. The locale argument is a string that specifies the language and region to be used for the date formatting, while the options argument is an object that specifies the formatting options.

For example, to format the date created above in the US English locale with the short date format, you can use the following code:

```javascript
let formattedDate = date.toLocaleDateString('en-US', {
  day: 'numeric',
  month: 'short',
  year: 'numeric'
});

// Output: 4/20/2020
```

##### Converting to Other Date Formats

Once the date has been formatted using the `toLocaleDateString()` method, it can then be converted to other date formats as needed. For example, if you need to convert the formatted date to the ISO 8601 format, you can use the `toISOString()` method, as shown below:

```javascript
let isoDate = date.toISOString();

// Output: 2020-04-20T00:00:00.000Z
```

Alternatively, if you need to convert the formatted date to a UNIX timestamp, you can use the `getTime()` method, as shown below:

```javascript
let unixTimestamp = date.getTime();

// Output: 1587371200000
```
