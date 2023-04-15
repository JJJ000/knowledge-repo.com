---
title: What is the proper way to format a Microsoft json date?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `\/Date()\/` format to format a Microsoft JSON date.
---

**Contents**

[TOC]

### Introduction

Microsoft JSON dates are a specific type of date format used in JSON files. They are used to store dates in the form of a string, and they follow a specific pattern to ensure the date is properly formatted. In this article, we will discuss how to format a Microsoft JSON date in JSON.

### Formatting a Microsoft JSON Date

To format a Microsoft JSON date in JSON, you will need to use the following pattern:

```json
"\/Date(<timestamp>+<offset>)\/"
```

Where `<timestamp>` is the number of milliseconds since the Unix Epoch (January 1, 1970 00:00:00 UTC) and `<offset>` is the time offset from UTC in minutes.

### Example

For example, if we wanted to format the date April 14, 2021 at 10:00 AM UTC, we would use the following pattern:

```json
"\/Date(1618454400000+0)\/"
```

### Conclusion

In conclusion, formatting a Microsoft JSON date in JSON is a simple process that involves using a specific pattern. By following this pattern, you can easily format any date in the Microsoft JSON format.
