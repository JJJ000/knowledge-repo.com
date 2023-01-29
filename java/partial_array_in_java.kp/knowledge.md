---
title: How can I access a portion of an array in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the Arrays.copyOfRange() method to get only part of an array in Java.
---

**Contents**

[TOC]

1. Using Arrays.copyOfRange() 
   - Syntax: `Arrays.copyOfRange(originalArray, startIndex, endIndex);`
   - Description: This method returns a new array containing the elements from the original array ranging from the startIndex (inclusive) to the endIndex (exclusive).
2. Using System.arraycopy() 
   - Syntax: `System.arraycopy(originalArray, startIndex, newArray, 0, length);`
   - Description: This method copies the elements of the original array starting from the startIndex to the newArray of length specified.
3. Using for loop 
   - Syntax: 
   ```java
   int[] newArray = new int[length];
   for (int i = startIndex; i < endIndex; i++) {
      newArray[i - startIndex] = originalArray[i];
   }
   ```
   - Description: This method uses a for loop to iterate through the original array from the startIndex to the endIndex, and assigns the elements to the new array.
4. Using subList() 
   - Syntax: `List<Integer> newList = originalList.subList(startIndex, endIndex);`
   - Description: This method returns a view of the portion of the original list between the startIndex (inclusive) and the endIndex (exclusive). This view can be converted to an array using the toArray() method.
