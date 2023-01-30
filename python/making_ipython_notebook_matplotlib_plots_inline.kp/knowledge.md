---
title: How to display matplotlib plots within an ipython notebook
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the %matplotlib inline magic command.
---

**Contents**

[TOC]

**Section 1: Setting up the Environment**

First, you will need to ensure that the IPython notebook and matplotlib are installed in your environment. IPython notebook can be installed using pip, and matplotlib can be installed using either pip or conda.

**Section 2: Configuring the IPython Notebook**

Once the environment is set up, you will need to configure the IPython notebook to display the plots inline. This can be done by adding the following line of code to the beginning of the notebook:

```
%matplotlib inline
```

**Section 3: Generating a Plot**

Now that the environment is set up and configured, you can generate a plot using matplotlib. To do this, simply import the matplotlib library and use the `plot()` function to generate the plot.

**Section 4: Displaying the Plot**

Finally, to display the plot inline, simply call the `show()` function. This will display the plot inline in the IPython notebook.
