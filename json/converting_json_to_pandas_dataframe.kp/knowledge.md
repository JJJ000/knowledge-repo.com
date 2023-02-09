---
title: Converting a JSON file into a pandas dataframe
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The pandas library provides a function called `read\_json` which can be used to convert a JSON string to a pandas DataFrame.
---

**Contents**

[TOC]

**Section 1: Import Libraries**

In order to convert a JSON to a pandas DataFrame, we need to first import the necessary libraries. This can be done using the following code:

```python
import pandas as pd
import json
```

**Section 2: Load JSON File**

The next step is to load the JSON file. This can be done by using the `json.load()` method. The following code can be used to load the JSON file:

```python
with open('data.json') as json_file:
    data = json.load(json_file)
```

**Section 3: Convert JSON to DataFrame**

Once the JSON file is loaded, we can use the `pd.DataFrame()` method to convert the JSON data into a pandas DataFrame. The following code can be used to perform this conversion:

```python
df = pd.DataFrame(data)
```

**Section 4: View DataFrame**

Finally, we can view the DataFrame by using the `df.head()` method. This will display the first five rows of the DataFrame. The following code can be used to view the DataFrame:

```python
df.head()
```
