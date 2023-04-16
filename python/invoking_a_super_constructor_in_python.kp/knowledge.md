---
title: What is the syntax for calling the parent class constructor in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In Python, the super() function can be used to invoke the super constructor.
---

**Contents**

[TOC]

# Invoking the Super Constructor

## Step 1: Create a Superclass
The first step in invoking the super constructor is to create a superclass. This can be done by creating a class that has the desired attributes and methods.

## Step 2: Create a Subclass
The next step is to create a subclass that inherits the attributes and methods from the superclass. This can be done by using the `class` keyword and specifying the superclass as the parent class.

## Step 3: Invoke the Super Constructor
Once the subclass has been created, the super constructor can be invoked by using the `super()` method. This method takes the subclass as its first argument, followed by any additional arguments that are needed for the super constructor.

## Step 4: Call the Subclass Constructor
Finally, the subclass constructor can be called to initialize the object. This can be done by using the `__init__()` method, which takes the necessary arguments for the subclass constructor.
