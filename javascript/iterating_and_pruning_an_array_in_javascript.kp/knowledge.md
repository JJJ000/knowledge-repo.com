---
title: Iterating over an array and deleting elements without disrupting the for loop
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Using the Array.prototype.splice() method to remove items from the array during the loop iteration.
---

**Contents**

[TOC]

**Section 1: Using a Temporary Array**

In this approach, we can use a temporary array to store the items that we want to remove from the original array. We can then loop through the original array and check if the current item is in the temporary array. If it is, we can skip over it and move on to the next item. If the item is not in the temporary array, then we can add it to a new array. This new array will contain all the elements from the original array, minus the ones that we wanted to remove.

**Section 2: Using the splice() Method**

Another approach is to use the splice() method. This method allows us to remove elements from an array without breaking the for loop. We can loop through the array and check if the current item is one that we want to remove. If it is, we can call the splice() method on the array and pass in the index of the item that we want to remove. This will remove the item from the array and shift all the other elements down one index.

**Section 3: Using the filter() Method**

The filter() method is another way to remove elements from an array without breaking the for loop. This method allows us to pass in a callback function that will be used to filter out unwanted elements. We can loop through the array and check if the current item is one that we want to remove. If it is, we can call the filter() method on the array and pass in a callback function that will return false for the item that we want to remove. This will remove the item from the array and return a new array with all the remaining elements.

**Section 4: Using the delete Operator**

The delete operator can also be used to remove elements from an array without breaking the for loop. We can loop through the array and check if the current item is one that we want to remove. If it is, we can call the delete operator on the array and pass in the index of the item that we want to remove. This will remove the item from the array and shift all the other elements down one index. However, it should be noted that this approach does not actually remove the item from the array, it just sets the value to undefined.
