---
title: What is causing date.parse to provide inaccurate results?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Date.parse gives incorrect results in Javascript because it does not take into account timezones or daylight savings time.
---

**Contents**

[TOC]

# Reasons for Incorrect Results 

Date.parse is a method in JavaScript that is used to parse a date string and return the number of milliseconds since January 1, 1970. It is often used to convert date strings into date objects. However, it can sometimes produce incorrect results due to the following reasons:

# Lack of Standardization 

The main reason for incorrect results from Date.parse is the lack of standardization in the format of date strings. Different browsers and JavaScript engines can interpret date strings differently, resulting in different results. For example, some browsers may interpret the date string "01/02/2019" as January 2nd, 2019 while others may interpret it as February 1st, 2019.

# Time Zone Differences 

Another reason for incorrect results is time zone differences. Date.parse assumes that the date string is in the local time zone, which may not be the case. If the date string is in a different time zone, the results may be incorrect. For example, if the date string is in the Pacific time zone, Date.parse may interpret it as if it were in the Eastern time zone, resulting in an incorrect result.

# Invalid Date Strings 

Finally, Date.parse can produce incorrect results if the date string is invalid. For example, if the date string is missing a day or month, the results may be incorrect. Additionally, Date.parse does not support all date formats, so if the date string is in an unsupported format, the results may be incorrect.
