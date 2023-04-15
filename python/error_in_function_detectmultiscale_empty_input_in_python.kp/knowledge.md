---
title: There is an error in the detectmultiscale function with code (-215) that indicates the input is not empty
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: This error occurs when the input image passed to the detectMultiScale function is empty (has no pixels).
---

**Contents**

[TOC]

Section 1: Introduction
The error "(-215) !empty() in function detectMultiScale" typically occurs when the input image in a face detection algorithm is empty or has not been properly loaded. Essentially, the algorithm is trying to detect faces in an image that does not exist.

Section 2: Troubleshooting Steps
To troubleshoot this error, you can perform the following steps:
1. Check that the file path to the image is correct and that the image actually exists.
2. Ensure that you are using the correct file type for the image (e.g., .jpg, .png).
3. Verify that the image has been correctly loaded into the algorithm by printing it out or displaying it.
4. Check the format of the image before passing it to the detectMultiScale function. It should be in grayscale.

Section 3: Sample Code
Here is a sample code that demonstrates how this error can occur:

```
import cv2

img_path = 'path_to_image.jpg'

# Load the image
img = cv2.imread(img_path)

# Convert to grayscale
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Detect faces
face_cascade = cv2.CascadeClassifier('haarcascade_frontalface_alt.xml')
faces = face_cascade.detectMultiScale(gray)

# Display the image with detected faces
for (x,y,w,h) in faces:
    cv2.rectangle(img,(x,y),(x+w,y+h),(255,0,0),2)

cv2.imshow('img',img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

Section 4: Conclusion
In conclusion, the error "(-215) !empty() in function detectMultiScale" can usually be resolved by verifying that the input image has been properly loaded into the algorithm and is in the correct format before passing it to the detectMultiScale function.
