---
title: Which values can be used as valid tags in the "freq" parameter of pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Values that are valid in Pandas `Freq` tags in Python include string aliases for time offsets (such as `H` for hourly, `D` for daily), integer offsets, and a timedelta object.
---

**Contents**

[TOC]

### Introduction
Pandas library is used in Python to perform various tasks such as data manipulation, data analysis, data visualization. Pandas provide various APIs to work with dates and times. In pandas, we have a concept of frequency, also known as 'Freq'. The 'Freq' is used to represent the frequency of the data, such as monthly, yearly, weekly, etc. In this article, we will discuss the valid values that we can use with the Pandas 'Freq' tags in Python.

### Valid values in Pandas 'Freq' tags
Below is the list of valid values that we can use with the Pandas 'Freq' tags:

1. Date offset aliases
    - B: Business day frequency.
    - D: Calendar day frequency.
    - H: Hourly frequency.
    - T, min: Minutely frequency.
    - S: Secondly frequency.
    - L, ms: Millisecond frequency.
    - U, us: Microsecond frequency.
    - N: Nanosecond frequency.

2. Weekday offset aliases
    - W-SUN: Weekly on Sunday.
    - W-MON: Weekly on Monday.
    - W-TUE: Weekly on Tuesday.
    - W-WED: Weekly on Wednesday.
    - W-THU: Weekly on Thursday.
    - W-FRI: Weekly on Friday.
    - W-SAT: Weekly on Saturday.

3. Month offset aliases
    - MS: Month start frequency.
    - M: Month end frequency.
    - BM: Business month end frequency.
    - CBM: Custom business month end frequency.
    - MS: Month start frequency.
    - WMS: Weekly start of month.
    - WOM: Week of month.
    - Q-JAN: Quarterly, year ending in January.
    - Q-FEB: Quarterly, year ending in February.
    - Q-MAR: Quarterly, year ending in March.
    - Q-APR: Quarterly, year ending in April.
    - Q-MAY: Quarterly, year ending in May.
    - Q-JUN: Quarterly, year ending in June.
    - Q-JUL: Quarterly, year ending in July.
    - Q-AUG: Quarterly, year ending in August.
    - Q-SEP: Quarterly, year ending in September.
    - Q-OCT: Quarterly, year ending in October.
    - Q-NOV: Quarterly, year ending in November.
    - Q-DEC: Quarterly, year ending in December.
    - BQ-JAN: Business quarterly, year ending in January.
    - BQ-FEB: Business quarterly, year ending in February.
    - BQ-MAR: Business quarterly, year ending in March.
    - BQ-APR: Business quarterly, year ending in April.
    - BQ-MAY: Business quarterly, year ending in May.
    - BQ-JUN: Business quarterly, year ending in June.
    - BQ-JUL: Business quarterly, year ending in July.
    - BQ-AUG: Business quarterly, year ending in August.
    - BQ-SEP: Business quarterly, year ending in September.
    - BQ-OCT: Business quarterly, year ending in October.
    - BQ-NOV: Business quarterly, year ending in November.
    - BQ-DEC: Business quarterly, year ending in December.
    - QS-JAN: Quarterly, year starting in January.
    - QS-FEB: Quarterly, year starting in February.
    - QS-MAR: Quarterly, year starting in March.
    - QS-APR: Quarterly, year starting in April.
    - QS-MAY: Quarterly, year starting in May.
    - QS-JUN: Quarterly, year starting in June.
    - QS-JUL: Quarterly, year starting in July.
    - QS-AUG: Quarterly, year starting in August.
    - QS-SEP: Quarterly, year starting in September.
    - QS-OCT: Quarterly, year starting in October.
    - QS-NOV: Quarterly, year starting in November.
    - QS-DEC: Quarterly, year starting in December.
    - BQS-JAN: Business quarterly, year starting in January.
    - BQS-FEB: Business quarterly, year starting in February.
    - BQS-MAR: Business quarterly, year starting in March.
    - BQS-APR: Business quarterly, year starting in April.
    - BQS-MAY: Business quarterly, year starting in May.
    - BQS-JUN: Business quarterly, year starting in June.
    - BQS-JUL: Business quarterly, year starting in July.
    - BQS-AUG: Business quarterly, year starting in August.
    - BQS-SEP: Business quarterly, year starting in September.
    - BQS-OCT: Business quarterly, year starting in October.
    - BQS-NOV: Business quarterly, year starting in November.
    - BQS-DEC: Business quarterly, year starting in December.
    
4. Anchored offsets
    - A: Year end frequency (December).
    - BA: Business year end frequency.
    - AS: Year start frequency (January).
    - BAS: Business year start frequency.
    - BH: Business hour frequency.
    - BY: Year end frequency (use last business day frequency).
    - BYS: Year start frequency (use first business day frequency).
    - C: Custom business day frequency.
    
### Conclusion
In this article, we have discussed the valid values that we can use with the Pandas 'Freq' tags in Python. The 'Freq' is used to represent the frequency of the data, such as monthly, yearly, weekly, etc. Pandas provide various APIs to work with dates and times, which makes it easy to manipulate and analyze data with time-series.
