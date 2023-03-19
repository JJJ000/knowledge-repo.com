---
title: What is the method to generate a file name that includes the current date and time using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the datetime module to retrieve the current date and time, and format it as desired for the file name.
---

**Contents**

[TOC]

Section 1: Getting the current date and time in Python

To create a file name with the current date and time in Python, we first need to get the current date and time. We can use the datetime module in Python to get the current date and time. Here's how:

```python
import datetime

now = datetime.datetime.now()
print("Current date and time: ")
print(now)
```

This will give us the current date and time in the format: YYYY-MM-DD HH:MM:SS.ssssss

Section 2: Formatting the current date and time

Now that we have the current date and time, we need to format it to use it as a file name. We can use the strftime() method to format the date and time. Here's an example:

```python
import datetime

now = datetime.datetime.now()
formatted_date_time = now.strftime("%Y-%m-%d_%H-%M-%S")
print("Formatted date and time: ")
print(formatted_date_time)
```

This will give us the current date and time in the format: YYYY-MM-DD_HH-MM-SS

Section 3: Creating a file name with the current date and time

Now that we have the formatted date and time, we can use it to create a file name. Here's how we can create a file name with the current date and time:

```python
import datetime

now = datetime.datetime.now()
formatted_date_time = now.strftime("%Y-%m-%d_%H-%M-%S")
file_name = f"file_{formatted_date_time}.txt"
print("File name with current date and time: ")
print(file_name)
```

This will give us a file name with the current date and time in the format: file_YYYY-MM-DD_HH-MM-SS.txt

Section 4: Writing to a file with the current date and time

If we want to create a file with the current date and time and write some text to it, we can do it like this:

```python
import datetime

now = datetime.datetime.now()
formatted_date_time = now.strftime("%Y-%m-%d_%H-%M-%S")
file_name = f"file_{formatted_date_time}.txt"

with open(file_name, 'w') as f:
    f.write("This is some text that we want to write to the file.")
```

This will create a file with the current date and time as the file name and write the text "This is some text that we want to write to the file." to the file.
