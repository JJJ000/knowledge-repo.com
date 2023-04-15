---
title: What is the process for verifying if a key is present in **kwargs?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: One way to check if a key exists in **kwargs dictionary in Python is by using the in operator.
---

**Contents**

[TOC]

## Section 1: Introduction to **kwargs in Python

In Python, `**kwargs` is a special syntax used for passing a keyworded, variable-length argument list to a function. It is a way to accept any number of keyword arguments in a function.

The `**kwargs` syntax allows the passing of a dictionary of key-value pairs where the keyword is the key, and the argument is value. It makes the code flexible and easy to read.


## Section 2: Checking if a Key in **kwargs exists

To check if a key in `**kwargs` exists, we can use the `in` keyword. It returns `True` if the key is present in the `**kwargs` dictionary and `False` if it is not present.

Here is an example:

```python
def my_function(**kwargs):
    if 'key_name' in kwargs:
        print("Key exists in **kwargs")
    else:
        print("Key does not exist in **kwargs")
```

In the above example, we define a function that accepts `**kwargs` as a parameter. We check if the key `'key_name'` exists in the dictionary using the `in` keyword. If the key exists, we print `"Key exists in **kwargs"`. Otherwise, we print `"Key does not exist in **kwargs"`.


## Section 3: Example of how to check if a key exists in **kwargs

Let's take a look at an example that uses the above function:

```python
def main():
    my_function(key_name='value')
    my_function(another_key='value')

if __name__ == '__main__':
    main()
```

In the `main` function, we call `my_function` twice. The first time, we pass `'key_name'` as a key in `**kwargs`, and the second time, we pass `'another_key'`. The output of running the above code would be:

```
Key exists in **kwargs
Key does not exist in **kwargs
```


## Section 4: Conclusion

In conclusion, checking if a key in `**kwargs` exists in Python is a straightforward task. We use the `in` keyword to check if the key is present in the `**kwargs` dictionary or not. This allows for flexible and easy-to-read code.
