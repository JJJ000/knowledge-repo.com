---
title: What is the correct JSON date format?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The `right` JSON date format in Javascript is ISO 8601 (YYYY-MM-DDTHHmmss.sssZ).
---

**Contents**

[TOC]

1. ISO 8601 Format
The "right" JSON date format in Javascript is the ISO 8601 format, which is a standardized international format for representing dates and times. It is the most widely accepted format and is the format used by the JavaScript Date object. The ISO 8601 format is a string in the form of `YYYY-MM-DDTHH:mm:ss.sssZ`, where `YYYY` is the four-digit year, `MM` is the two-digit month, `DD` is the two-digit day, `HH` is the two-digit hour, `mm` is the two-digit minute, `ss` is the two-digit second, and `sss` is the three-digit millisecond. The `Z` at the end indicates that the time is in UTC.

2. Date Object
The Date object in JavaScript is used to represent dates and times. It can be used to parse strings in the ISO 8601 format and create Date objects from them. The Date object also has methods for formatting dates and times into strings in the ISO 8601 format.

3. Other Formats
Although the ISO 8601 format is the most widely accepted and is the format used by the JavaScript Date object, there are other formats that can be used in JSON. These formats include RFC 3339, which is a simplified version of the ISO 8601 format, as well as Unix timestamps, which are integers representing the number of seconds since January 1, 1970.

4. Custom Formats
It is also possible to use custom date formats in JSON. These formats must be explicitly specified and can be any string that can be parsed into a Date object. However, it is not recommended to use custom date formats as they are not as widely accepted and may lead to confusion or errors.
