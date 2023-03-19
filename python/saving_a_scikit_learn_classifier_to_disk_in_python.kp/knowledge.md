---
title: Storing the classifier in scikit-learn to the hard drive
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can save classifiers to disk in scikit-learn using the `joblib` module`s dump() function.
---

**Contents**

[TOC]

## Section 1: Introduction to Classifier in scikit-learn

Scikit-learn is a popular Python library that provides efficient tools for data mining and machine learning. It offers various algorithms for classification, regression, clustering, dimensionality reduction, and model selection. In this context, a classifier is a function that learns to predict the class label of a given input data.

## Section 2: Saving Classifier to Disk

Once a machine learning model (classifier) is trained, it must be saved to be used later for prediction on new data. Scikit-learn provides a simple method called `joblib.dump` to save the classifier object to a file on disk. This method is preferred over Python's `pickle` module because it is more efficient for large NumPy arrays.

```python
import joblib

# Train the classifier model
classifier.fit(X_train, y_train)

# Save the classifier to disk
joblib.dump(classifier, 'classifier_file.joblib')
```

In the code above, we imported the `joblib` module and trained a classifier model (`classifier`) using the `fit` method. After that, we saved the classifier to a file called `classifier_file.joblib` on disk using `joblib.dump`.


## Section 3: Loading Classifier from Disk

To use the saved classifier later, we need to load it from disk. This can be done easily using `joblib.load` method. Once the classifier object is loaded, we can make predictions on new data.

```python
# Load the saved classifier from disk
clf = joblib.load('classifier_file.joblib')

# Predict on new data
y_pred = clf.predict(X_test)
```

In the code above, we loaded the classifier object from the file `classifier_file.joblib` using `joblib.load`. After that, we used the loaded classifier object (`clf`) to predict the class label of new data (`X_test`).

## Conclusion

Saving and loading classifier objects is an essential task for production deployment after the classifier model is trained. In this tutorial, we learned how to use the `joblib` module to save and load a classifier object from disk. We must keep in mind that the disk space and memory required to store the classifier model depend on the size of the data and the complexity of the model.
