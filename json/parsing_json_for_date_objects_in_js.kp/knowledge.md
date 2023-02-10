---
title: What is the process for converting JSON data into a date object in javascript?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the Date constructor to parse the JSON string into a Date object.
---

**Contents**

[TOC]

# Section 1 - Formatting the Date
The date needs to be formatted in the JSON string as a string in ISO 8601 format. This format looks like "YYYY-MM-DDTHH:mm:ssZ", where "YYYY" is the 4-digit year, "MM" is the 2-digit month, "DD" is the 2-digit day, "HH" is the 2-digit hour, "mm" is the 2-digit minute, and "ss" is the 2-digit second. An example of this format is "2016-09-16T15:30:00Z".

# Section 2 - Parsing the Date
Once the date is formatted correctly, it can be parsed using the JavaScript Date object. To do this, the Date object's constructor can be used, passing in the ISO 8601 string as an argument. The constructor will return a Date object representing the date and time specified in the string.

# Section 3 - Accessing the Date Object
Once the Date object has been created, the various date and time components can be accessed using the various methods provided by the Date object. For example, the getFullYear() method can be used to get the 4-digit year, the getMonth() method can be used to get the month (0-11), and the getDate() method can be used to get the day of the month (1-31).

# Section 4 - Formatting the Date
Once the Date object has been created and the various components have been accessed, the date can be formatted for display. This can be done using the toLocaleDateString() method, which takes a locale as an argument and returns a string representation of the date in the specified locale.
