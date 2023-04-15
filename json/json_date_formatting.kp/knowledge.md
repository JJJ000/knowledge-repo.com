---
title: What is the correct json date format?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The correct JSON date format is `YYYY-MM-DDThh:mm:ss.sssZ`, where `T` is a literal character separating the date and time, and `Z` indicates the time is in UTC.
---

**Contents**

[TOC]

### ISO 8601
The most common and accepted standard for representing dates and times in JSON is the ISO 8601 format. This format is a combination of the ISO date and time formats, and is used to represent dates and times in a machine-readable way. The format is based on the Coordinated Universal Time (UTC) and takes the form of `YYYY-MM-DDThh:mm:ssZ`, where YYYY is the four-digit year, MM is the two-digit month, DD is the two-digit day, hh is the two-digit hour, mm is the two-digit minute, and ss is the two-digit second.

### RFC 3339
The RFC 3339 format is an updated version of ISO 8601 and is used to represent dates and times in a human-readable way. This format is based on the Internet Date/Time Format and takes the form of `YYYY-MM-DDThh:mm:ss+hh:mm`, where YYYY is the four-digit year, MM is the two-digit month, DD is the two-digit day, hh is the two-digit hour, mm is the two-digit minute, and ss is the two-digit second.

### Unix Time
Unix time is a system for representing time as a single number, and is used to represent dates and times in a machine-readable way. This format is based on the Unix epoch time and takes the form of a 10-digit integer, which represents the number of seconds since January 1, 1970, 00:00:00 UTC.

### JavaScript Date Object
The JavaScript Date object is used to represent dates and times in a human-readable way. This format is based on the JavaScript Date object and takes the form of a string, which represents the date and time in the local time zone.
