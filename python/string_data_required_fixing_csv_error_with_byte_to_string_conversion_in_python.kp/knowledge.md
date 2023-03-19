---
title: The error message 'csv.error iterator should provide strings instead of bytes' should be rephrased
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The CSV file needs to be opened in binary mode (`rb`) or the strings should be decoded from bytes.
---

**Contents**

[TOC]

Section 1: Background
When working with CSV files, it is very common to encounter the error "csv.Error: iterator should return strings, not bytes". This error can occur when attempting to read a CSV file using the csv Python module. 

Section 2: Explanation of Error
The reason for this error is that the csv module in Python expects the iterator passed to it to return strings, not bytes. However, if the iterator returns binary data, the csv module will throw an error. 

Section 3: Solution
One way to solve this issue is to ensure that the data being passed to the csv module is in string format. One way to achieve this is by using the "utf-8" encoding when reading the CSV file. To do this, simply add the encoding parameter to the open() function. For example:

```
with open('example.csv', 'r', encoding='utf-8') as csv_file:
    csv_reader = csv.reader(csv_file)
```

Alternatively, if you have binary data that needs to be converted to string format before it can be passed to the csv module, you can use the decode() method to accomplish this. For example:

```
with open('example.csv', 'rb') as csv_file:
    csv_reader = csv.reader((line.decode('utf-8') for line in csv_file))
```

Section 4: Conclusion
In conclusion, the "csv.Error: iterator should return strings, not bytes" error can be frustrating and confusing, but it is easily addressed by ensuring that the data being passed to the csv module is in string format. This can be achieved using the "utf-8" encoding or the decode() method to convert binary data to strings.
