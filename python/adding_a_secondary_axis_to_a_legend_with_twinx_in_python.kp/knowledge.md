---
title: How can I include the secondary axis in the legend using twinx()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can add the secondary axis to the legend by calling ax.legend() after creating the twinx() axes.
---

**Contents**

[TOC]

#### Create a Legend

To create a legend for a secondary axis with twinx(), use the ax.legend() method. This method allows you to specify the legend’s location, title, and labels for each item in the legend. For example, the following code adds a legend to the secondary axis with twinx():

```
# Create legend
ax.legend(loc='upper left', title='Legend', labels=['Data 1', 'Data 2'])
```

#### Specify the Legend Location

The ax.legend() method allows you to specify the location of the legend. The location is specified using a string or a tuple of two numbers. The string can be one of the following values: ‘best’, ‘upper right’, ‘upper left’, ‘lower left’, ‘lower right’, ‘right’, ‘center left’, ‘center right’, ‘lower center’, ‘upper center’, or ‘center’. Alternatively, you can specify the location as a tuple of two numbers, which represent the x and y coordinates of the legend’s lower left corner.

#### Specify the Legend Title

The ax.legend() method allows you to specify the title of the legend. The title is specified using a string. For example, the following code adds a title to the legend:

```
# Specify legend title
ax.legend(title='Legend Title')
```

#### Specify the Legend Labels

The ax.legend() method allows you to specify the labels for each item in the legend. The labels are specified using a list of strings. For example, the following code adds labels to the legend:

```
# Specify legend labels
ax.legend(labels=['Data 1', 'Data 2'])
```
