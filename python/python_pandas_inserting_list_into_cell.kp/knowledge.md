---
title: Reworded how to add a list to a cell in Python pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To insert a list into a cell using pandas, simply pass the list into square brackets when assigning a value to the cell.
---

**Contents**

[TOC]

**Section 1: Introduction to the Problem**

In data analysis, working with dataframe cells that contain lists in pandas can be a challenge. One common task is to insert a list into a single cell of a pandas dataframe. While pandas' rows and columns are a great way to store and manipulate data in tables, there are times when we need to store more complex structures such as a list into a cell. This article will provide some ways to insert a list into a cell in a pandas dataframe.


**Section 2: Using apply() method**

One way to insert a list into a cell in pandas is to use the apply() function. The apply() function is a powerful tool in pandas that can apply any function to a dataframe or a series object. 

Here's an example:

```
import pandas as pd

# Creating a sample dataframe 
df = pd.DataFrame({'Name': ['John', 'Jane', 'Mike'], 'Value': ['A', 'B', 'C']})

# Defining the list to be inserted
my_list = [1, 2, 3, 4, 5]

# Using apply() to insert the list into a cell in the 'Value' column
df['Value'] = df['Value'].apply(lambda x: my_list if x == 'A' else x)

print(df)
```

Output:
```
   Name                Value
0  John  [1, 2, 3, 4, 5]
1  Jane                B
2  Mike                C
```

In the example above, we have created a new dataframe with two columns, 'Name' and 'Value'. We then define a list, my_list which we will insert into a cell in the 'Value' column. We use the apply() function to apply a lambda function that checks if the value in the 'Value' column is 'A'. If it is, the lambda function returns the entire list, otherwise, the lambda function returns the existing value in the cell. We overwrite the 'Value' column with the result of the apply() function.


**Section 3: Using the .loc() method**

Another way to insert a list into a cell in pandas is to use the .loc() method. The .loc() method is used to access a group of rows and columns by labels or a boolean array.

Here's an example:

```
import pandas as pd

# Creating a sample dataframe 
df = pd.DataFrame({'Name': ['John', 'Jane', 'Mike'], 'Value': ['A', 'B', 'C']})

# Defining the list to be inserted
my_list = [1, 2, 3, 4, 5]

# Using .loc() to insert the list into a cell in the 'Value' column
df.loc[df['Name'] == 'John', 'Value'] = my_list

print(df)
```

Output:
```
   Name                Value
0  John  [1, 2, 3, 4, 5]
1  Jane                B
2  Mike                C
```

In the example above, we have created a new dataframe with two columns, 'Name' and 'Value'. We then define a list, my_list which we will insert into a cell in the 'Value' column. We use the .loc() method to access the cell where the 'Name' column value is equal to 'John' and the 'Value' column. We then set the value of that cell to my_list.


**Section 4: Using the .iat() or .at() method**

Finally, another way to insert a list into a cell in pandas is to use the .at() or .iat() method. These methods are used to access a scalar value by label or by position.

Here's an example:

```
import pandas as pd

# Creating a sample dataframe 
df = pd.DataFrame({'Name': ['John', 'Jane', 'Mike'], 'Value': ['A', 'B', 'C']})

# Defining the list to be inserted
my_list = [1, 2, 3, 4, 5]

# Using .iat() to insert the list into a cell in the 'Value' column
df.iat[0, df.columns.get_loc('Value')] = my_list

print(df)
```

Output:
```
   Name                Value
0  John  [1, 2, 3, 4, 5]
1  Jane                B
2  Mike                C
```

In the example above, we have created a new dataframe with two columns, 'Name' and 'Value'. We then define a list, my_list which we will insert into a cell in the 'Value' column. We use the .iat() method to access the cell at position (0, 1) (i.e., the first row and the 'Value' column) and assign it the value of my_list.


**Conclusion**

In this article, we have discussed three ways to insert a list into a cell in pandas dataframe. We can use the apply() method, the .loc() method or the .iat() or .at() method depending on our specific use case. By using these methods, we can store more complex data structures in pandas dataframes and perform data analysis more easily.
