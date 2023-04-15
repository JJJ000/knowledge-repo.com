---
title: Convert the empty values to empty strings instead of nan while using pandas.read_csv
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Add the parameter `na\_filter=False` to the pandas.read\_csv() statement.
---

**Contents**

[TOC]

Section 1: Introduction
In pandas, read_csv() method is used to read a CSV file and convert it to a DataFrame. By default, read_csv() method converts any empty value in the CSV file to NaN (Not a Number). However, in some cases, we may want to read empty values as empty strings instead of NaN. This can be achieved by providing specific parameters to the read_csv() method.

Section 2: Using the na_filter parameter
The na_filter parameter of the read_csv() method is used to specify whether to detect and convert empty values to NaN or not. By default, na_filter parameter is set to True, which means that empty values are detected and converted to NaN. To read empty values as empty strings, we need to set the na_filter parameter to False. Here is the example code:

```
import pandas as pd

# Set na_filter to False
df = pd.read_csv('example.csv', na_filter=False)

# Display the DataFrame
print(df)
```

In this example, the read_csv() method will read the example.csv file and will not convert any empty values to NaN. Instead, it will read them as empty strings.

Section 3: Using the keep_default_na and na_values parameters
Alternatively, we can also use the keep_default_na and na_values parameters of the read_csv() method to achieve the same result. The keep_default_na parameter is used to specify whether to keep the default NaN values or not. The na_values parameter is used to specify the values to be treated as NaN. Here is the example code:

```
import pandas as pd

# Set keep_default_na and na_values parameters
df = pd.read_csv('example.csv', keep_default_na=False, na_values=[''])

# Display the DataFrame
print(df)
```

In this example, the read_csv() method will read the example.csv file and will treat empty values as NaN only if they are not explicitly included in the na_values list. Since an empty string is explicitly included in the na_values list, it will be treated as an empty string instead of NaN.

Section 4: Conclusion
In this tutorial, we have seen two ways to read empty values as empty string instead of NaN in pandas. The first way is to set the na_filter parameter of the read_csv() method to False. The second way is to set the keep_default_na and na_values parameters of the read_csv() method to False and [''], respectively. By using one of these ways, we can easily read empty values as empty string in a pandas DataFrame.
