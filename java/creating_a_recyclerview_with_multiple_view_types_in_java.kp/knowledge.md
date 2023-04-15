---
title: How to make a recyclerview with multiple item layouts
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Create a RecyclerView Adapter that implements getItemViewType() and onCreateViewHolder() to inflate multiple view types.
---

**Contents**

[TOC]

1. **Create Model Class:** 
   Create a model class to store the data that will be displayed in the RecyclerView.

2. **Implement Multiple View Types:**
   Create a custom adapter that extends RecyclerView.Adapter and implement multiple view types. Override the getItemViewType() method to return the different view types and inflate the corresponding view in the onCreateViewHolder() method.

3. **Bind Data to Views:**
   In the onBindViewHolder() method, bind the data from the model class to the corresponding views.

4. **Set Adapter to RecyclerView:**
   Create an instance of the custom adapter and set it to the RecyclerView.
