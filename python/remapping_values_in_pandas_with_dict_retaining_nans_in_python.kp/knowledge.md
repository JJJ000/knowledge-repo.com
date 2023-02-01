---
title: Replace the values in a pandas column using a dictionary, while keeping any nan values unchanged
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the `na\_action` parameter of the `map` method to specify `ignore` in order to preserve NaNs when remapping the values in a pandas column with a dict.
---

**Contents**

[TOC]

### Creating a Dictionary 
We can create a dictionary to remap the values in a pandas column. The keys of the dictionary will be the values that we want to remap, and the values will be the new values that we want to assign. 

For example, if we have a column of pet names, and we want to remap them to the names of their respective species, we can create a dictionary like this:

```
name_map = {
    'Fido': 'Dog',
    'Max': 'Dog',
    'Fluffy': 'Cat',
    'Garfield': 'Cat'
}
```

### Using the Dictionary 
Once we have our dictionary, we can use it to remap the values in our pandas column. To do this, we can use the `.map()` method on the column, passing in our dictionary as an argument.

For example, if we have a pandas column called `pet_name`, we can remap the values using the dictionary we created above like this:

```
df['pet_name'] = df['pet_name'].map(name_map)
```

### Preserving NaNs
By default, the `.map()` method will replace any NaN values in the column with `NaN`. To preserve the NaNs, we can set the `na_action` parameter to `'ignore'`. This will cause the `.map()` method to ignore any NaN values, leaving them unchanged.

For example, if we have a pandas column called `pet_name`, we can remap the values and preserve the NaNs like this:

```
df['pet_name'] = df['pet_name'].map(name_map, na_action='ignore')
```
