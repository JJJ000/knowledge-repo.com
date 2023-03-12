---
title: What is the process of copying sys.stdout to a log file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: By redirecting the output with sys.stdout to a file object created for the log file in write mode.
---

**Contents**

[TOC]

## Importing Required Modules

The first step is to import the required modules to create and write to a log file. In this case, we will use the 'sys' and 'os' module.

```python
import sys
import os
```

## Creating the Log File

After importing the required modules, we can create a function to create and open a log file in write mode. The function will take the file path as an argument.

```python
def create_log_file(file_path):
    log_dir = os.path.dirname(file_path)
    if not os.path.exists(log_dir):
        os.makedirs(log_dir)

    sys.stdout = open(file_path, mode='w')
```

In the above code, we create a directory for the log file to be saved to if it does not already exist. After creating the directory, we open the log file in write mode using the file path provided as an argument. Finally, we assign the 'sys.stdout' to the log file.

## Duplicating sys.stdout to Log File

To duplicate the 'sys.std.out' to the log file created, we can simply print to the console and the log file at the same time.

```python
print('Hello World!')
```

After executing the 'Hello World!' print statement, the log file should also contain the same output.

## Restoring sys.stdout

After usage, it is good practice to restore 'sys.stdout' back to its original value to avoid errors in future cases where 'sys.stdout' is used.

```python
sys.stdout.close()
sys.stdout = sys.__stdout__
```

The above code restores the 'sys.stdout' back to its original value by closing the log file and assigning the original 'sys.stdout' back to 'sys.stdout'.

## Final Code

The final code should look similar to the below.


```python
def create_log_file(file_path):
    log_dir = os.path.dirname(file_path)
    if not os.path.exists(log_dir):
        os.makedirs(log_dir)

    sys.stdout = open(file_path, mode='w')


def main():
    create_log_file('logs/my_log.txt')
    print('Hello World!')
    sys.stdout.close()
    sys.stdout = sys.__stdout__


if __name__ == "__main__":
    main()
```


In the 'main' function above, we call the 'create_log_file' function to create the log file. We then print 'Hello World!' to the console and log file. Finally, we restore 'sys.stdout' back to its original value by closing the log file and assigning it to 'sys.__stdout__'.
