---
title: What is the process for saving and restoring a model after training?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Save a model after training in Python by using the model`s `save` method, and restore a model by using the model`s `load` method.
---

**Contents**

[TOC]

## Saving the Model

The easiest way to save a trained model in Python is to use the `pickle` module. Pickle is a module that serializes (converts a Python object into a string) any Python object, so that it can be saved to a file and later restored.

To save a model, you must first open a file in write mode, then call the `pickle.dump()` method and pass in the model and the file object.

```python
import pickle

# Open a file to save the model
model_file = open('model.pkl', 'wb')

# Save the model
pickle.dump(model, model_file)

# Close the file
model_file.close()
```

## Restoring the Model

To restore a saved model, you must first open the file in read mode, then call the `pickle.load()` method and pass in the file object.

```python
import pickle

# Open the file to load the model
model_file = open('model.pkl', 'rb')

# Load the model
model = pickle.load(model_file)

# Close the file
model_file.close()
```

Once the model is restored, you can use it to make predictions or continue training.
