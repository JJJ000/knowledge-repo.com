---
title: Retrieving particular columns from a numpy array
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To extract specific columns in numpy array in Python, use the indexing syntax [, columns] where `columns` specify the column numbers to extract.
---

**Contents**

[TOC]

Section 1: Introduction 
In data analysis, it is common to work with large datasets that contain many attributes or features. In some scenarios, we might only be interested in a few specific columns of the dataset. In this case, we can extract the desired columns using NumPy arrays. 

Section 2: Loading a dataset into a NumPy array 
To load a dataset into a NumPy array, we can use the loadtxt() function from the NumPy library. This function takes in the file path and a delimiter (usually a comma for CSV files) as parameters. 

```
import numpy as np
data = np.loadtxt('dataset.csv', delimiter=',')
```
We can also use the genfromtxt() function which can handle missing values (denoted by NaN or n/a) and headers. 

```
import numpy as np
data = np.genfromtxt('dataset.csv', delimiter=',', missing_values=['NaN', 'n/a'], skip_header=1)
```

Section 3: Extracting specific columns 
To extract specific columns from the array, we can use indexing. The syntax for indexing a NumPy array is array[row_index, column_index]. We can use a colon (:) to select all rows or columns. 

For example, to extract the first and third columns of the data array, we can use the following code: 

```
import numpy as np
data = np.loadtxt('dataset.csv', delimiter=',')
specific_columns = data[:, [0, 2]]
```

Section 4: Saving the extracted columns 
After extracting the desired columns, we might want to save them to a new file. We can do this using the savetxt() function from NumPy. This function takes in the file path and an array as parameters. 

```
import numpy as np
data = np.loadtxt('dataset.csv', delimiter=',')
specific_columns = data[:, [0, 2]]
np.savetxt('specific_columns.csv', specific_columns, delimiter=',')
```
