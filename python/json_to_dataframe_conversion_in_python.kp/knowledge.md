---
title: Transforming JSON into a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the pandas library`s `read\_json()` function to convert JSON data to a pandas DataFrame in Python.
---

**Contents**

[TOC]

**Section 1: Introduction**

JSON (JavaScript Object Notation) is a lightweight data interchange format used widely by web applications for data exchange. JSON data can be easily converted into pandas DataFrame in Python, which provides an easy way to perform data analysis on the JSON data.

In this tutorial, we will discuss how to convert JSON data to pandas DataFrame in Python. 

**Section 2: Loading JSON data into Python**

Before we can convert JSON data into pandas DataFrame, we first need to load the JSON data into Python. There are multiple ways to load JSON data into Python, including:

- Using json library: The json library in Python provides a simple way to load JSON data into Python using the loads() function.

- Using pandas library: The pandas library provides a read_json() function that can be used to load JSON data directly into a pandas DataFrame.

- Using urllib and json library: If the JSON data is available online, we can use the urllib library to fetch the data and the json library to load the data into Python.

Here is an example code for loading JSON data using the json library:

```
import json

# JSON data
data = '{"name": "John", "age": 30, "city": "New York"}'

# Loading JSON data into Python
json_data = json.loads(data)

print(json_data)
```

Output:
```
{'name': 'John', 'age': 30, 'city': 'New York'}
```

**Section 3: Converting JSON data to pandas DataFrame**

Once we have loaded the JSON data into Python, we can easily convert it into a pandas DataFrame using the pandas library.

Here is an example code for converting JSON data to pandas DataFrame:
```
import pandas as pd
import json

# JSON data
data = '[{"name": "John", "age": 30, "city": "New York"}, {"name": "Jane", "age": 25, "city": "Los Angeles"}, {"name": "Bob", "age": 40, "city": "Chicago"}]'

# Loading JSON data into Python
json_data = json.loads(data)

# Converting JSON data to pandas DataFrame
df = pd.DataFrame(json_data)

print(df)
```

Output:
```
   age         city  name
0   30     New York  John
1   25  Los Angeles  Jane
2   40      Chicago   Bob
```
In this example, we used the loads() function to load the JSON data into Python and then used the DataFrame() function of pandas library to create a DataFrame from the JSON data.

**Section 4: Conclusion**

Converting JSON data to pandas DataFrame in Python is a simple task that can be accomplished using the json library and the pandas library. By doing so, we can easily perform data analysis on the JSON data using the vast number of data analysis tools available in pandas.
