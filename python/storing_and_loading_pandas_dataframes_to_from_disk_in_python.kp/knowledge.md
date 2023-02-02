---
title: Saving and retrieving a pandas dataframe to/from disk in a reversible way
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: To reversibly store and load a Pandas dataframe to/from disk in Python, use the Pandas to\_pickle() and read\_pickle() methods.
---

**Contents**

[TOC]

### Storing a Pandas Dataframe to Disk

The `to_pickle()` method of a Pandas DataFrame can be used to store the dataframe to disk. This method serializes the dataframe and stores it in a file using the Python pickle serialization format.

```python
df.to_pickle(file_name)
```

### Loading a Pandas Dataframe from Disk

The `read_pickle()` method of the Pandas library can be used to load the dataframe from disk. This method deserializes the dataframe from the pickle file.

```python
df = pd.read_pickle(file_name)
```

### Reversibility

The Python pickle serialization format is reversible, meaning that the dataframe can be stored and loaded back in its original form. This makes it a useful format for storing and loading Pandas dataframes.

### Advantages

The pickle format is easy to use and provides a convenient way to store and load Pandas dataframes. It is also reversible, meaning that the dataframe can be stored and loaded back in its original form. This makes it a useful format for storing and loading Pandas dataframes.
