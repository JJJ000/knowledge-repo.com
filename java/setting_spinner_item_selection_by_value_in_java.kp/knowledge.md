---
title: What is the method for selecting an item in a spinner based on its value, rather than its position?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the setSelection(int index) method of the Spinner class, passing the index of the item in the adapter corresponding to the desired value.
---

**Contents**

[TOC]

1. **Creating a Map**
To set the selected item of a Spinner by value, instead of by position, the values of the Spinner must first be mapped to a data structure such as a Map. This can be done by looping through the items in the Spinner's adapter and creating a Map that maps the item's value to its position in the adapter.

2. **Retrieving the Position**
Once the Map has been created, the position of the desired value can be retrieved by querying the Map. This can be done by calling `Map.get(value)` with the desired value as the parameter.

3. **Setting the Position**
Once the position of the desired value has been retrieved, it can be set as the selected item of the Spinner. This can be done by calling `Spinner.setSelection(position)` with the retrieved position as the parameter.

4. **Example Code**
Below is an example of code that sets the selected item of a Spinner by value:

```java
// Get the Spinner and its adapter
Spinner spinner = findViewById(R.id.spinner);
ArrayAdapter<String> adapter = (ArrayAdapter<String>) spinner.getAdapter();

// Create a Map that maps values to positions
Map<String, Integer> spinnerMap = new HashMap<String, Integer>();
for (int i = 0; i < adapter.getCount(); i++) {
    spinnerMap.put(adapter.getItem(i), i);
}

// Retrieve the position of the desired value
String value = "My Value";
int position = spinnerMap.get(value);

// Set the position as the selected item of the Spinner
spinner.setSelection(position);
```
