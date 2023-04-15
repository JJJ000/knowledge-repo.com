---
title: Verify if the list of objects comprises an object that possesses a definite attribute value
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To check if a list of objects contains an object with a certain attribute value in Python, you can use a list comprehension and the `any()` function to return a Boolean value.
---

**Contents**

[TOC]

1. Introduction

In Python, there are different ways to check if a list of objects contains an object with a certain attribute value. In this guide, we will explore some of these methods.

2. Using a for loop and if statement

One way to check if a list of objects contains an object with a certain attribute value in Python is by using a for loop and an if statement. Here is an example:

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

person1 = Person("Alice", 25)
person2 = Person("Bob", 30)
person3 = Person("Charlie", 35)

people = [person1, person2, person3]

for person in people:
    if person.name == "Bob":
        print("Bob found!")
```

In this example, we have a class called `Person` with two attributes: `name` and `age`. We create three `Person` objects and add them to a list called `people`. We then use a for loop to iterate over each `Person` object in `people`. Inside the loop, we check if the current `Person` object has a `name` attribute equal to `"Bob"`. If so, we print a message indicating that `"Bob"` was found.

3. Using list comprehension

Another way to check if a list of objects contains an object with a certain attribute value in Python is by using list comprehension. Here is an example:

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

person1 = Person("Alice", 25)
person2 = Person("Bob", 30)
person3 = Person("Charlie", 35)

people = [person1, person2, person3]

bob_found = any(person.name == "Bob" for person in people)

if bob_found:
    print("Bob found!")
```

In this example, we use the same `Person` class and `people` list as before. We use list comprehension to create a list of Boolean values indicating whether each `Person` object has a `name` attribute equal to `"Bob"`. We then use the `any()` function to check if there is at least one `True` value in the list. If so, we print a message indicating that `"Bob"` was found.

4. Using filter() method

A third way to check if a list of objects contains an object with a certain attribute value in Python is by using the `filter()` method. Here is an example:

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

person1 = Person("Alice", 25)
person2 = Person("Bob", 30)
person3 = Person("Charlie", 35)

people = [person1, person2, person3]

filtered_people = list(filter(lambda person: person.name == "Bob", people))

if filtered_people:
    print("Bob found!")
```

In this example, we again use the `Person` class and `people` list. We use the `filter()` method with a lambda function that checks if each `Person` object has a `name` attribute equal to `"Bob"`. We then convert the filtered result to a list and check whether the resulting list is not empty. If it is not empty, we print a message indicating that `"Bob"` was found.
