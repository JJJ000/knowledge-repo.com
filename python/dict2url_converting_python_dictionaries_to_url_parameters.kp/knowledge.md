---
title: Conversion of Python dictionary into url parameters
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the urllib.parse.urlencode() method to convert a Python dictionary to URL parameters.
---

**Contents**

[TOC]

Section 1: Introduction
In web development, parameters or query strings are used to pass data to the server in the URL. Sometimes, we may have a dictionary object in Python that we want to convert to URL parameters before sending it to the server. In this article, we will look at how we can convert a Python dictionary to URL parameters (query strings).

Section 2: Converting a Python Dictionary to URL Parameters
To convert a Python dictionary to URL parameters, we can use the urllib.parse module which provides a urlencode() function. 

Here's an example:

```
import urllib.parse

my_dict = {'name': 'John', 'age': 30, 'city': 'New York'}

query_string = urllib.parse.urlencode(my_dict)

print(query_string)

# Output: name=John&age=30&city=New+York
```

As we can see from the code, we first import the urllib.parse module. Then, we create a dictionary object with some sample data. Next, we use the urlencode() function to convert the dictionary to a URL query string. Finally, we print the query string.

Section 3: Special Characters
When converting a dictionary to URL parameters, we need to be careful about special characters. For example, if our dictionary contained a string value with special characters, such as a question mark or an ampersand, then those characters may interfere with the query string. 

To avoid this problem, we can use the quote() function from the same urllib.parse module to encode any special characters in the values of the dictionary. 

Here's an example:

```
import urllib.parse

my_dict = {'name': 'John', 'age': 30, 'city': 'New?York'}

for key, value in my_dict.items():
    my_dict[key] = urllib.parse.quote(str(value))

query_string = urllib.parse.urlencode(my_dict)

print(query_string)

# Output: name=John&age=30&city=New%3FYork
```

As we can see from the code, we first import the urllib.parse module. Then, we create a dictionary object with some sample data, including a special character in the city key. Next, we iterate over the dictionary items and use the quote() function to encode any special characters. Finally, we use the urlencode() function to convert the dictionary to a URL query string and print the result.

Section 4: Conclusion
In this article, we have looked at how we can convert a Python dictionary to URL parameters. We have seen that we can use the urlencode() function from the urllib.parse module to achieve this. We have also discussed how to handle special characters in the dictionary values to ensure that the resulting query string is valid.
