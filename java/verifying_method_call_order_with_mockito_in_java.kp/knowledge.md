---
title: Verify that mockito is following the correct sequence of method calls
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Mockito can verify that methods are called in a specific order using the inOrder() method.
---

**Contents**

[TOC]

## Using Mockito
Mockito provides an easy way to verify the order and sequence of method calls using the `inOrder` method.

### Step 1: Create the Mock Object
Create the mock object of the class whose method calls you want to verify.

### Step 2: Create an InOrder Object
Create an `InOrder` object with the mock object created in Step 1.

### Step 3: Call the Methods
Call the methods of the class whose order you want to verify.

### Step 4: Verify the Order
Call the `verify` method of the `InOrder` object created in Step 2, passing in the methods that you called in Step 3. This will verify that the methods were called in the order that you specified.
