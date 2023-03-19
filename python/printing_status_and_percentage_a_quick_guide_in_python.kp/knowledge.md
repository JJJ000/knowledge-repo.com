---
title: What is the process for displaying a status bar and percentage in printed output?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: One way to print out a status bar and percentage in Python is by using the tqdm library.
---

**Contents**

[TOC]

## Section 1: Introduction

For many applications that involve lengthy computations, it is important to provide feedback to the user on the progress of the computation. One common way to do this is to display a status bar or progress bar. In this tutorial, we will learn how to implement a simple status bar in Python that displays the progress of a loop as a percentage.

## Section 2: Code example

Here is an example of how to implement a simple status bar in Python:

```python
import time

total = 1000
for i in range(total):
    progress = (i + 1) / total
    bar_length = 20
    progress_bar = '[' + '#' * int(progress * bar_length) + '-' * (bar_length - int(progress * bar_length)) + ']'
    percent = '{:.1%}'.format(progress)
    status = '\r{} {} {}'.format(progress_bar, percent, 'processing...')
    print(status, end='')
    time.sleep(0.05)

print('\n')
```

This code uses the `time` module to add a small delay between each iteration of the loop, so that we can see the status bar being updated. The loop iterates a total of 1000 times, and on each iteration, it calculates the progress of the loop as a percentage. It then constructs a progress bar string, and formats it with the percentage and a status message. Finally, it prints the status message using the `\r` character to overwrite the previous line, so that the status bar appears to be updating in real-time.

## Section 3: Explanation

Let's go through the code line by line to understand how it works:

```python
import time
```

We import the `time` module, which provides a `sleep` function that we will use to add a small delay between each iteration of the loop.

```python
total = 1000
for i in range(total):
```

We set a variable `total` to the number of iterations that we want to perform, and then iterate over a range of numbers from 0 to `total - 1`.

```python
progress = (i + 1) / total
```

On each iteration, we calculate the progress of the loop as a decimal between 0 and 1, by dividing the current iteration number `i + 1` by the total number of iterations `total`. We add 1 to `i` before dividing because Python ranges start at 0.

```python
bar_length = 20
progress_bar = '[' + '#' * int(progress * bar_length) + '-' * (bar_length - int(progress * bar_length)) + ']'
```

We set a variable `bar_length` to the number of characters that we want the progress bar to be. We then create a progress bar string using the `#` character to represent completed progress, and the `-` character to represent incomplete progress. We use the `int` function to round the progress percentage down to the nearest integer, and multiply it by `bar_length` to get the number of `#` characters to include in the progress bar. We subtract that from `bar_length` to get the number of `-` characters to include in the progress bar.

```python
percent = '{:.1%}'.format(progress)
```

We format the progress as a percentage string with one decimal place using Python's `str.format` method.

```python
status = '\r{} {} {}'.format(progress_bar, percent, 'processing...')
```

We create a status message string by formatting the progress bar, the percentage, and a status message using the `\r` character at the beginning of the string. The `\r` character tells Python to overwrite the previous line, so that the status bar appears to be updating in real-time.

```python
print(status, end='')
```

We print the status message without adding a newline to the end, so that the next iteration of the loop will overwrite the previous output.

```python
time.sleep(0.05)
```

We add a small delay of 50 milliseconds between each iteration of the loop, to make the status bar update more slowly and be easier to read.

```python
print('\n')
```

Finally, we print a newline character at the end of the loop to move the cursor to the next line, so that the output of the program is cleanly formatted.

## Section 4: Conclusion

In this tutorial, we learned how to implement a simple status bar in Python that displays the progress of a loop as a percentage. We used string formatting, the `print` function, and the `\r` character to overwrite the previous line of output, so that the status bar appeared to be updating in real-time. This is a useful technique when running long calculations or simulations, as it provides feedback to the user on the progress of the computation.
