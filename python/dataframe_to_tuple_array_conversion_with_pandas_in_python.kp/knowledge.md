---
title: Transforming a dataframe into an array consisting of tuples in pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To convert a Pandas dataframe to an array of tuples in Python, you can use the to\_records() method.
---

**Contents**

[TOC]

Section 1: Introduction
In this task, we need to convert a pandas dataframe to an array of tuples in Python. The array of tuples can be useful for iterating over rows in the dataframe or for transferring data to other functions that require tuples as inputs. In this tutorial, we will learn how to convert a pandas dataframe to an array of tuples using different methods.

Section 2: Using the to_records() Method
One way to convert a pandas dataframe to an array of tuples is to use the to_records() method. This method converts each row of the dataframe to a tuple and then combines all tuples in an array. Here is how to use it:

```
import pandas as pd

df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
array_of_tuples = [tuple(x) for x in df.to_records(index=False)]
print(array_of_tuples)
```

Output:
```
[(1, 4), (2, 5), (3, 6)]
```

In this code, we first create a pandas dataframe with two columns (A and B) and three rows. Then, we use the to_records() method to convert the dataframe to a NumPy structured array. Finally, we convert the structured array to a list of tuples by iterating over each row of the array and converting it to a tuple using the tuple() function.

Section 3: Using the itertuples() Method
Another way to convert a pandas dataframe to an array of tuples is to use the itertuples() method. This method returns an iterator yielding namedtuples for each row in the dataframe. Here is how to use it:

```
import pandas as pd

df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
array_of_tuples = [tuple(row[1:]) for row in df.itertuples()]
print(array_of_tuples)
```

Output:
```
[(1, 4), (2, 5), (3, 6)]
```

In this code, we first create a pandas dataframe with two columns (A and B) and three rows. Then, we use the itertuples() method to iterate over each row of the dataframe and return a namedtuple for that row. We use tuple slicing to exclude the index number from the namedtuple and convert it to a tuple.

Section 4: Conclusion
In conclusion, we have learned how to convert a pandas dataframe to an array of tuples using two different methods: to_records() and itertuples(). Both methods provide an easy way to convert a dataframe to an array of tuples that can be used for further processing. It is up to personal preference which method to choose, as both methods produce the same output.
