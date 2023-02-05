---
title: Encoding labels in multiple columns using scikit-learn
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: scikit-learn`s MultiLabelBinarizer can be used to encode labels across multiple columns.
---

**Contents**

[TOC]

##### Section 1: Preprocessing

Label encoding is a preprocessing technique used to convert categorical data into numerical data. It is commonly used in machine learning algorithms to convert categorical features into numerical features. In scikit-learn, the LabelEncoder class can be used to encode categorical features into numerical features.

##### Section 2: LabelEncoder Class

The LabelEncoder class in scikit-learn can be used to encode labels with value between 0 and n_classes-1. It can be used to encode multiple columns in a dataset. The fit() method can be used to fit the LabelEncoder to the dataset and the transform() method can be used to transform the labels into numerical values.

##### Section 3: Example

For example, consider a dataset with three columns - 'Gender', 'Country' and 'Age'. The Gender column has two labels - 'Male' and 'Female', the Country column has three labels - 'India', 'USA' and 'UK' and the Age column has five labels - '18-25', '26-35', '36-45', '46-55' and '56-65'.

To encode these labels using the LabelEncoder class, first create an instance of the LabelEncoder class. Then, call the fit() method on the instance and pass the dataset as the argument. This will fit the LabelEncoder to the dataset. Finally, call the transform() method on the instance and pass the dataset as the argument. This will transform the labels into numerical values.

##### Section 4: Output

The output of the LabelEncoder will be a dataset with numerical values instead of labels. For example, the Gender column will have values 0 and 1, the Country column will have values 0, 1 and 2 and the Age column will have values 0, 1, 2, 3 and 4.
