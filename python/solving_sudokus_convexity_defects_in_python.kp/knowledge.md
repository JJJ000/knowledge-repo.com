---
title: What is the technique for eliminating convexity flaws in a sudoku grid?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the convex hull and find the largest contour to remove the convexity defects in a Sudoku square in Python.
---

**Contents**

[TOC]

## Introduction
Sudoku is a popular logic-based number placement game that requires filling a 9x9 grid with digits so that each column, each row, and each of the nine 3x3 subgrids contains all of the digits from 1 to 9. In some cases, the input Sudoku square can have convexity defects, which are cells that are surrounded by cells of higher or equal values, making it impossible to place a digit in that cell. In this tutorial, we will discuss how to remove such convexity defects in a Sudoku square using Python.

## Prerequisites
Before we proceed with the implementation, make sure to install the following packages:
- numpy
- opencv-python
- imutils

## Methodology
We will use the following approach to remove convexity defects in a Sudoku square:
1. Read the input image of the Sudoku square using OpenCV.
2. Convert the image to grayscale and apply thresholding to obtain a binary image.
3. Perform morphological operations such as erosion and dilation to remove noise and fill gaps in the image.
4. Find the contours in the image and iterate through each contour.
5. For each contour, check if it contains convexity defects using the cv2.convexityDefects() function.
6. Remove the convexity defects by drawing a line from the start point to the end point of each defect.
7. Display the resulting image.

Let's see the implementation of each step in Python code.

## Implementation
```python
import cv2
import numpy as np
import imutils

# Step 1: Read the input image
img = cv2.imread('sudoku.jpg')
img = imutils.resize(img, height=400) # resize the image for better visualisation

# Step 2: Convert to grayscale and apply thresholding
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
thresh = cv2.adaptiveThreshold(gray, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY_INV, 11, 2)

# Step 3: Perform morphological operations
kernel = np.ones((3,3), np.uint8)
thresh = cv2.erode(thresh, kernel, iterations=1)
thresh = cv2.dilate(thresh, kernel, iterations=1)

# Step 4: Find the contours
cnts = cv2.findContours(thresh.copy(), cv2.RETR_EXTERNAL, cv2.CHAIN_APPROX_SIMPLE)
cnts = imutils.grab_contours(cnts)

# Step 5: Remove convexity defects
for c in cnts:
    hull = cv2.convexHull(c, returnPoints=True) # find the convex hull
    defects = cv2.convexityDefects(c, cv2.convexHull(c, returnPoints=True)) # find the convexity defects
    
    if defects is None: # no defects found
        continue
    
    for i in range(defects.shape[0]):
        s,e,f,d = defects[i, 0]
        start = tuple(c[s][0])
        end = tuple(c[e][0])
        far = tuple(c[f][0])
        
        # check if the defect is valid
        if d > 10000: # adjust the threshold if required
            continue
        
        # draw a line from the start point to the end point of the defect
        cv2.line(img, start, end, (0,255,0), 2)

# Step 6: Display the image
cv2.imshow("Sudoku", img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Conclusion
In this tutorial, we have discussed how to remove convexity defects in a Sudoku square using Python. This technique can be useful in automating the process of solving Sudoku puzzles. However, it is important to note that this approach may not work for all types of convexity defects, and may require additional preprocessing to detect and remove such defects.
