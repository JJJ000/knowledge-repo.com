---
title: What is the formula for converting seconds into hours, minutes, and seconds?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can convert seconds to hours, minutes and seconds in Python using the divmod() function.
---

**Contents**

[TOC]

# Section 1: Import Necessary Libraries

import math

# Section 2: Define Function 

def convert_seconds(seconds):
    hours = math.floor(seconds / 3600)
    minutes = math.floor((seconds - (hours * 3600)) / 60)
    remaining_seconds = seconds - (hours * 3600) - (minutes * 60)
    return "%d:%02d:%02d" % (hours, minutes, remaining_seconds)

# Section 3: Call Function

seconds = 86400
print(convert_seconds(seconds))

# Section 4: Output

Output: 24:00:00
