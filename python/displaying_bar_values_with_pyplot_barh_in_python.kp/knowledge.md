---
title: What is the method to exhibit the bar value on individual bars using pyplot.barh()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `plt.text()` function to add the value of each bar as a label to the corresponding bar in a horizontal bar chart created using `pyplot.barh()`.
---

**Contents**

[TOC]

## Section 1: Introduction

In Python, `pyplot.barh()` is a function used to plot a horizontal bar plot. It is commonly used to display categorical data with their corresponding values. However, it might be challenging to understand the exact value of each bar without looking at their values on the y-axis.

In this tutorial, we will learn how to display the value of each bar on the bar plot using `pyplot.barh()` in Python.


## Section 2: Displaying Value on Each Bar

To display the value of each bar on the bar plot, we can use the `text()` function of Matplotlib. This function allows us to add arbitrary text to the plot. 

Let's consider the following example where we have a dictionary containing the values of different programming languages:

```python
import matplotlib.pyplot as plt

languages = {'Python': 30, 'Java': 20, 'C++': 10, 'JavaScript': 25, 'PHP': 15}

# plotting a horizontal bar with pyplot.barh()
plt.barh(range(len(languages)), list(languages.values()), align='center')
plt.yticks(range(len(languages)), list(languages.keys()))

plt.show()
```

This will produce a horizontal bar plot with the different programming languages on the y-axis and their corresponding values on the x-axis.

To display the values of each bar on the plot, we can modify the code to use the `text()` function as shown:

```python
import matplotlib.pyplot as plt

languages = {'Python': 30, 'Java': 20, 'C++': 10, 'JavaScript': 25, 'PHP': 15}

# plotting a horizontal bar with pyplot.barh()
plt.barh(range(len(languages)), list(languages.values()), align='center')
plt.yticks(range(len(languages)), list(languages.keys()))

# displaying the value of each bar
for i, v in enumerate(languages.values()):
    plt.text(v + 1, i, str(v), color='blue', fontweight='bold')

plt.show()
```

In this code, we have added a for loop that iterates over the values of the `languages` dictionary. For each value, we use the `text()` function to display the value of the bar just to the right of the bar. The `plt.text()` function takes the `x`, `y`, and `text` parameters, where `x` is the position of the text, `y` is the vertical position of the text, and `text` is the string that we want to display on the plot. In this case, we have also set the color of the text to blue and the font weight to bold.


## Section 3: Result

If we execute the final code, we should see a horizontal bar plot with the value of each bar displayed on it. The resulting plot will look something like this:

![Bar Graph with values](https://github.com/ossamaAhmed/ossamaAhmed/blob/main/Images/Bar%20Graph%20with%20values.png)

As we can see, the value of each bar is displayed just to the right of the bar in blue color and bold font. This makes it much easier to understand the exact value of each bar.


## Section 4: Conclusion

In this tutorial, we have learned how to display the value of each bar on a horizontal bar plot using `pyplot.barh()` in Python. By using the `text()` function of Matplotlib, we can add arbitrary text to the plot, including the value of each bar. This allows us to create more informative plots that are easier to understand.
