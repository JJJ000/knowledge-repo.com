---
title: Converting a date to a JSON string using the json.stringify() method alters the time of the date due to the fact that it uses universal coordinated time (utc)
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Yes, JSON Stringify changes the time of date due to UTC being used for serializing and deserializing dates.
---

**Contents**

[TOC]

## Yes

When a JavaScript Date object is serialized to a JSON string, the Date object is converted to a string in the UTC format. This means that the Date object's time value is converted to the number of milliseconds since January 1, 1970 00:00:00 UTC. This can cause the time value of the Date object to be different than the time value when it was first created.

## No

When the JSON string is parsed back into a Date object, the time value is converted back to the local time zone. This means that the time value of the Date object will be the same as when it was first created. The only difference is that the time value is now in the local time zone instead of UTC.

## Impact

When a Date object is serialized to a JSON string, the time value can be changed. This can impact applications that rely on the time value being accurate. For example, a calendar application may rely on the time value being accurate when displaying events.

## Solution

To ensure that the time value of the Date object is preserved when serializing to a JSON string, the time value should be stored separately. This can be done by storing the time value in a separate field in the JSON string. This will ensure that the time value is preserved when the JSON string is parsed back into a Date object.
