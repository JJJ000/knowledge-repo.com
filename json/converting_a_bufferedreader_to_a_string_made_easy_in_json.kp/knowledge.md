---
title: What is the simplest way to transform a bufferedreader into a string?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the BufferedReader`s readLine() method to read each line of the BufferedReader and append it to a StringBuilder, then use the StringBuilder`s toString() method to convert the BufferedReader to a String.
---

**Contents**

[TOC]

# Section 1: Determine Input Type
The first step to convert a BufferedReader to a String in Json is to determine the type of input. Depending on the type of input, different methods may be used to convert it to a String in Json. 

# Section 2: Convert to a String
Once the input type is known, the next step is to convert the BufferedReader to a String. This can be done by using the `readLine()` method of the BufferedReader class. This method reads in the data from the BufferedReader line by line, and stores it in a String. 

# Section 3: Parse the String
Once the data is stored in a String, it can be parsed using a Json parser. There are several Json parsers available, such as Gson and Jackson. These parsers can be used to convert the String into a Json object. 

# Section 4: Output the Json Object
The final step is to output the Json object. This can be done using the `toString()` method of the Json object. This will return a String representation of the Json object, which can then be used as desired.
