---
title: Importing a multi-line JSON file into pandas
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Pandas can be used to read in a file containing multiple lines of JSON into a DataFrame using the read\_json() function.
---

**Contents**

[TOC]

### Section 1: Load the JSON File

Pandas can load a file with more than one line of JSON using the `read_json` method. This method takes a file path as an argument and reads the JSON data into a DataFrame.

```
import pandas as pd

df = pd.read_json('path/to/file.json')
```

### Section 2: Parse the JSON Data

Once the JSON file is loaded into Pandas, it can be parsed into a DataFrame. This is done by specifying the orient parameter when calling the `read_json` method.

The orient parameter can take the following values:

- 'split' - Split the JSON file into columns
- 'records' - Load the data as a list of records
- 'index' - Use the field specified as the index
- 'columns' - Load the data as a dictionary of columns
- 'values' - Load the data as a list of values

For example, to parse the JSON data into a DataFrame with the 'index' orient:

```
df = pd.read_json('path/to/file.json', orient='index')
```

### Section 3: Access the Data

Once the JSON data is parsed into a DataFrame, it can be accessed using the standard DataFrame methods. For example, to access a specific column:

```
column_name = df['column_name']
```

Or to access a specific row:

```
row_index = df.loc[row_index]
```

### Section 4: Manipulate the Data

The DataFrame can also be manipulated using the standard DataFrame methods. For example, to add a new column:

```
df['new_column'] = some_data
```

Or to delete a column:

```
del df['column_name']
```
