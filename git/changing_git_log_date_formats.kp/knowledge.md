---
title: What are the different ways to format git log dates?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The Git log date format can be changed using the `--date` flag with the `log` command.
---

**Contents**

[TOC]

# Section 1: Changing the Date Format

Git allows you to customize the way it displays dates in the log output. To change the date format, you must use the “--date=<format>” option when running the “git log” command. 

# Section 2: Using the strftime Format

The “--date=<format>” option uses the strftime format for date strings. The strftime format is a standard way of expressing dates and times. It contains a set of characters that represent different parts of a date, such as the year, month, day, hour, minute, and second. 

# Section 3: Examples of Different Formats

Here are some examples of different formats you can use with the “--date=<format>” option: 

• %Y-%m-%d – YYYY-MM-DD format

• %a %b %d %H:%M:%S %Y – abbreviated weekday, month, day, hour, minute, second, and year

• %Y-%m-%d %H:%M:%S – YYYY-MM-DD HH:MM:SS format

# Section 4: Additional Resources

For more information about the strftime format and other date formats, you can refer to the official Git documentation or the strftime man page.
