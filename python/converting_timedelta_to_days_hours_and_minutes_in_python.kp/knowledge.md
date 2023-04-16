---
title: Express a timedelta as days, hours and minutes
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can convert a timedelta to days, hours and minutes by using the total\_seconds() method to convert the timedelta to seconds and then dividing the result by the number of seconds in a day, hour and minute, respectively.
---

**Contents**

[TOC]

#Convert to Days

timedelta_object = datetime.timedelta(days=4, hours=10, minutes=0)

days = timedelta_object.days

#Convert to Hours

hours = timedelta_object.seconds//3600

#Convert to Minutes

minutes = (timedelta_object.seconds//60) % 60

#Print Results

print("Days:", days)
print("Hours:", hours)
print("Minutes:", minutes)
