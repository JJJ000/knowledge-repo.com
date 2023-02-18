---
title: The argument provided to json_encode() contains an invalid utf-8 sequence
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: json\_encode() will return false if an invalid UTF-8 sequence is passed as an argument.
---

**Contents**

[TOC]

**Section 1: Overview**

json_encode() is a PHP function that takes a PHP value and encodes it into a JSON string. The function will throw an error if it encounters an invalid UTF-8 sequence in its argument. This error can be difficult to debug, as the invalid sequence is not always immediately obvious. 

**Section 2: Causes of Invalid UTF-8 Sequences**

Invalid UTF-8 sequences can be caused by a variety of factors. These include: 

* Incorrectly encoded data. For example, data that has been encoded with a different character set than the one intended. 

* Data that has been corrupted during transmission. 

* Data that has been modified by a program that is not UTF-8 aware.

**Section 3: How to Debug the Error**

The first step in debugging the error is to identify the source of the invalid UTF-8 sequence. This can be done by examining the data that is being passed to json_encode(). If the data is being read from a file, it can be checked to ensure that it is encoded correctly. If the data is being transmitted over a network, it can be checked for corruption. 

Once the source of the invalid UTF-8 sequence has been identified, it can be corrected and the json_encode() call can be re-executed. 

**Section 4: Conclusion**

When json_encode() throws an error due to an invalid UTF-8 sequence, it can be difficult to debug. However, by examining the data being passed to json_encode(), it is possible to identify the source of the invalid sequence and correct it. This will allow the json_encode() call to be re-executed without further errors.
