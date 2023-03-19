---
title: Convert a zipped file into a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To read a zipped file as a pandas DataFrame in Python, use the `pd.read\_csv()` function with the `compression=`zip`` parameter.
---

**Contents**

[TOC]

Section 1: Background
---------------------
Pandas is a popular data manipulation library in Python, which provides easy-to-use data structures and data analysis tools. One of the most common tasks in data analysis is reading data from a file. Pandas provides several methods to read data from various file formats such as CSV, Excel, JSON, SQL, and more. However, reading a zipped file is not directly supported by pandas, and we need to use additional libraries to read a zipped file as a pandas DataFrame. 

Section 2: Required Libraries
-----------------------------
To read a zipped file as a pandas DataFrame, we need to use the following libraries:

1. pandas - for data manipulation and DataFrame creation.
2. zipfile - for reading files from an archive.
3. io - for buffer management.

We can install these libraries using pip as follows:

```
pip install pandas zipfile io
```

Section 3: Reading a Zipped File as Pandas DataFrame
---------------------------------------------------
To read a zipped file as a pandas DataFrame, we can follow the following steps:

1. Import the required libraries:

```
import pandas as pd
import zipfile
import io
```

2. Read the zipped file into a buffer using the `zipfile` and `io` libraries:

``` 
with zipfile.ZipFile('path/to/archive.zip', 'r') as z:
    buffer = io.BytesIO(z.read('file_name.csv'))
```

3. Create a pandas DataFrame from the buffer:

```
df = pd.read_csv(buffer)
```

Here, we first open the zipped file using `ZipFile` and read a specific file from the archive using `read`. We then convert the file data into a bytes buffer using `io.BytesIO`. Finally, we create a DataFrame from the buffer using `pd.read_csv`. 

Section 4: Example
------------------
Let's see an example of reading a zipped CSV file as a pandas DataFrame:

```
import pandas as pd
import zipfile
import io

# read the zipped file into a buffer
with zipfile.ZipFile('sales.zip', 'r') as z:
    buffer = io.BytesIO(z.read('sales.csv'))

# create a pandas DataFrame from the buffer
df = pd.read_csv(buffer)

# print the first five rows of the DataFrame
print(df.head())
```

Here, we extract a file named `sales.csv` from a zipped file named `sales.zip`. We then create a DataFrame from the buffer using `pd.read_csv`. Finally, we print the first five rows of the DataFrame using `df.head()`.
