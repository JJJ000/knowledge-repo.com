---
title: What is the current screen orientation?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can get the current screen orientation in Java using the getOrientation() method of the Configuration class.
---

**Contents**

[TOC]

1. **Checking the Configuration**
The current screen orientation can be determined by checking the configuration of the device. This can be done by using the `getResources().getConfiguration()` method. This method will return an object of type `Configuration` which contains information about the device's configuration, including the current screen orientation.

2. **Retrieving the Orientation**
Once the configuration object has been obtained, the orientation can be retrieved by calling the `getOrientation()` method. This method will return an integer value indicating the current orientation. The possible values are `Configuration.ORIENTATION_PORTRAIT` and `Configuration.ORIENTATION_LANDSCAPE`.

3. **Handling Orientation Changes**
It is also possible to register a listener to be notified when the orientation changes. This can be done by using the `registerOnConfigurationChangedListener()` method. This method takes a `ConfigurationChangedListener` as an argument and will be called whenever the configuration of the device changes, including when the orientation changes.

4. **Example Code**
Below is an example of how to retrieve the current screen orientation and register a listener for orientation changes:

```java
// Get the current configuration
Configuration config = getResources().getConfiguration();

// Retrieve the current orientation
int orientation = config.getOrientation();

// Register a listener for orientation changes
config.registerOnConfigurationChangedListener(new ConfigurationChangedListener() {
    @Override
    public void onConfigurationChanged(Configuration newConfig) {
        // Retrieve the new orientation
        int newOrientation = newConfig.getOrientation();
        
        // Handle the orientation change
    }
});
```
