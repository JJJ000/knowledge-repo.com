---
title: What is the process for retrieving sharedpreferences from a preferenceactivity in android?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the getSharedPreferences() method of the PreferenceActivity.
---

**Contents**

[TOC]

####Section 1: Get a SharedPreferences Object

To get a SharedPreferences object from a PreferenceActivity in Android, use the getSharedPreferences() method. This method takes two parameters: a string that is the name of the file that will contain the preferences, and an integer that is the mode of the file.

For example, the following code will get a SharedPreferences object with the name "myPreferences" and the mode MODE_PRIVATE:

```
SharedPreferences prefs = getSharedPreferences("myPreferences", MODE_PRIVATE);
```

####Section 2: Access the SharedPreferences

Once you have the SharedPreferences object, you can access the preferences stored in it. To do this, use the getXXX() methods of the SharedPreferences object. The getXXX() methods take two parameters: a string that is the key of the preference, and a default value that will be returned if the key is not found.

For example, the following code will get the preference with the key "myKey" and a default value of "defaultValue":

```
String myValue = prefs.getString("myKey", "defaultValue");
```

####Section 3: Store Data in the SharedPreferences

To store data in the SharedPreferences object, use the edit() method to get an Editor object. The Editor object provides methods to store data in the SharedPreferences.

For example, the following code will store a string with the key "myKey" and the value "myValue":

```
Editor editor = prefs.edit();
editor.putString("myKey", "myValue");
editor.commit();
```

####Section 4: Retrieve Data from the SharedPreferences

To retrieve data from the SharedPreferences, use the getXXX() methods of the SharedPreferences object. The getXXX() methods take two parameters: a string that is the key of the preference, and a default value that will be returned if the key is not found.

For example, the following code will retrieve the preference with the key "myKey" and a default value of "defaultValue":

```
String myValue = prefs.getString("myKey", "defaultValue");
```
