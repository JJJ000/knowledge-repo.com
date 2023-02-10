---
title: What is the main goal of the @serializedname annotation when using gson in an Android application?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The @SerializedName annotation is used to map JSON keys to Java object fields when using Gson in Android.
---

**Contents**

[TOC]

# Introduction
The @SerializedName annotation is used to map a JSON field to a Java object field when using the Gson library in Android.

# Purpose
The purpose of this annotation is to allow the user to map a JSON field to a Java object field even if the names of the fields are not the same. This is useful for when the JSON field names are not the same as the Java object field names or if the JSON field names are not in the same format as the Java object field names.

# Advantages
Using the @SerializedName annotation has the advantage of allowing the user to easily map the JSON fields to the Java object fields without having to manually map each field. This saves time and makes the code more readable.

# Example
For example, if the JSON field name is "user_name" and the Java object field name is "userName", the @SerializedName annotation can be used to map the two fields like this:

@SerializedName("user_name")
String userName;
