---
title: How to calculate the amount of time it takes for a cell to run in an ipython notebook
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the %timeit magic command.
---

**Contents**

[TOC]

1. **Using the %time Magic Command**
The %time magic command is a simple and easy way to measure the execution time of a single line of code in a Jupyter Notebook. To use it, simply type %time before the code you want to measure:

```
%time
import numpy as np
a = np.random.rand(100)
```

2. **Using the %timeit Magic Command**
The %timeit magic command is similar to the %time command, but it runs the code multiple times to get a more accurate measure of the execution time. To use it, type %timeit before the code you want to measure:

```
%timeit
import numpy as np
a = np.random.rand(100)
```

3. **Using the %%timeit Cell Magic Command**
The %%timeit cell magic command is similar to the %timeit command, but it allows you to measure the execution time of an entire cell of code. To use it, type %%timeit at the beginning of the cell you want to measure:

```
%%timeit
import numpy as np
a = np.random.rand(100)
b = np.random.rand(100)
c = a + b
```

4. **Using the %%time Cell Magic Command**
The %%time cell magic command is similar to the %time command, but it allows you to measure the execution time of an entire cell of code. To use it, type %%time at the beginning of the cell you want to measure:

```
%%time
import numpy as np
a = np.random.rand(100)
b = np.random.rand(100)
c = a + b
```
