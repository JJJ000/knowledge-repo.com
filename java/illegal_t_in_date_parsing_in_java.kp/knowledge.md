---
title: An illegal character 't' was encountered when attempting to parse a date string into a java.util.date object
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The character `T` is not a valid pattern character for parsing a date string to java.util.Date.
---

**Contents**

[TOC]

## Overview
When attempting to parse a date string to a java.util.Date, the Illegal pattern character 'T' error may occur. This error occurs when the date string being parsed is not in the correct format. This article will explain what the error means and how to fix it.

## What is the Error?
The Illegal pattern character 'T' error occurs when the date string being parsed is not in the correct format. The 'T' character is used to separate the date and time components of a date string. If the 'T' character is not present, the date string will not be able to be parsed correctly and the error will be thrown.

## How to Fix the Error
The error can be fixed by ensuring that the date string is in the correct format. The date string should be in the ISO 8601 format, which is a standard for representing dates and times. The format is yyyy-MM-dd'T'HH:mm:ss.SSSZ, where yyyy is the year, MM is the month, dd is the day, HH is the hour, mm is the minute, ss is the second, SSS is the millisecond, and Z is the time zone. 

For example, a date string in the correct format would be: 2020-08-10T12:15:30.000+0500.

## Conclusion
The Illegal pattern character 'T' error occurs when the date string being parsed is not in the correct format. The date string should be in the ISO 8601 format, which is a standard for representing dates and times. Once the date string is in the correct format, the error should be resolved.
