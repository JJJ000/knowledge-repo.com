---
title: Save a numpy array as a csv file
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use numpy.savetxt() to dump a NumPy array into a csv file.
---

**Contents**

[TOC]

#Section 1: Create NumPy Array

import numpy as np 

arr = np.array([[1, 2, 3], [4, 5, 6]]) 

#Section 2: Create CSV File

import csv 

with open('filename.csv', 'w', newline='') as file: 
	writer = csv.writer(file) 
	writer.writerows(arr) 

#Section 3: Load CSV File

import csv 

with open('filename.csv', 'r') as file: 
	reader = csv.reader(file) 
	for row in reader: 
		print(row) 

#Section 4: Output

['1', '2', '3'] 
['4', '5', '6']
