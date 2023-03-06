---
title: What is the method to silence future warning in pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use the following code to suppress Pandas FutureWarning 
```
import warnings
warnings.filterwarnings(`ignore`, category=FutureWarning)
```
---

**Contents**

[TOC]

## Introduction

Pandas often shows FutureWarning that makes the user worry about the future implementation or to avoid the potential deprecation of functions in future releases. The warning message shows up when there's some change in a function or a method that might break the backward-compatibility in the forthcoming releases. There are many ways to suppress the FutureWarnings in Pandas that we will talk about in this tutorial.

## Issue with the FutureWarnings

Future Warnings make the user think about the command in use, and if it will quit working soon, it increases the anxiety of the user. Although they don't harm the system nor the command in use, they sometimes can cause the user to question their use, thus leading to frustration.

## Suppressing FutureWarnings

There are multiple ways to get over the warning shows in pandas outputs. Few of them are discussed below -

### Option 1 - Via filterwarnings method 

One way to suppress these warnings is to use a filterwarnings method that is implemented in the warnings module. It's best to use warning flag as once since you don't want to affect other warnings in your environment. Below is an example -


```python
import warnings
import pandas as pd

warnings.filterwarnings("once")

# suppress warning on this command
pd.DataFrame()

```

### Option 2 - Via Context Manager

Another way to suppress the FutureWarning is by using context managers. You can use the "with" statement to handle the warning. To use the "with" block statement with python, the method has to be usable as a context manager, and for that, warnings.simplefilter method can be used, as shown below -

```python
import pandas as pd
import warnings

# new dataframe
test = pd.DataFrame()

# handle the warning
with warnings.catch_warnings():
    warnings.simplefilter("ignore")
    
    pd.to_datetime(test)
```

### Option 3 - Via command line argument

If you execute the script on the command line, you can use the -W or -Wd option, -W takes action on any warning or errors, and using -Wd, you can selectively allow the warnings required, as shown below -

```python
python -W ignore script.py
```

### Option 4 - Modify Pandas Options

Another way to suppress FutureWarnings is to modify pandas options. The simplest way is to use the .option_context function that is context-aware using the following code:

```python
import pandas as pd
from pandas.core.common import SettingWithCopyWarning
import warnings

# modify pandas options to hide warnings
pd.set_option("mode.chained_assignment", None)
pd.options.mode.chained_assignment = None

test = pd.DataFrame()
with warnings.catch_warnings():
    warnings.simplefilter("ignore", category=SettingWithCopyWarning)
    
    test['a'] = 50

```

## Conclusion

The FutureWarnings are essential as they let the user know of upcoming changes, which might affect their code in the future. Removal of future warnings can be done avoiding problems that may arise in the future. We discussed various ways of how to disable or suppress FutureWarnings, so by suppressing them correctly, we can avoid unwanted noise that may crowd the display of the information that the developer will need.
