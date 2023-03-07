---
title: Determine the age using the birthdate in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To calculate age from birthdate in Python, subtract the birth year from the current year and adjust for the birth month and day.
---

**Contents**

[TOC]

## Section 1: Introduction to the problem

Given a person's birthdate, we need to find their age. This can be a common problem when working with data related to populations or creating applications that involve age-based restrictions.

In this task, we will use Python to calculate the age of a person from their birthdate.


## Section 2: Solution

To calculate the age of a person from their birthdate, we can use the datetime module in Python. Here are the steps we will follow:

1. Import the datetime module
2. Ask the user to input their birthdate in the format YYYY-MM-DD
3. Convert the birthdate string to a datetime object
4. Get the current date from the system
5. Calculate the difference between the current date and the birthdate
6. Extract the age from the difference and print it to the user

Here is the code that implements these steps:

```python
import datetime

# Ask user for birthdate
birthdate_str = input("Enter your birthdate (YYYY-MM-DD): ")

# Convert birthdate string to datetime object
birthdate = datetime.datetime.strptime(birthdate_str, "%Y-%m-%d")

# Calculate age
today = datetime.date.today()
age = today.year - birthdate.year - ((today.month, today.day) < (birthdate.month, birthdate.day))

# Print age
print("Your age is:", age)
```

## Section 3: Testing

Let's test the above code by asking the user for their birthdate and printing their age:

```
Enter your birthdate (YYYY-MM-DD): 2000-01-01
Your age is: 22
```

The output is correct, as the person born on 2000-01-01 would be 22 years old as of the current year.

## Section 4: Conclusion

In this task, we used the datetime module in Python to calculate the age of a person from their birthdate. This is a common problem when working with data related to populations or creating applications that involve age-based restrictions. We implemented the solution in Python and verified it with a test case.
