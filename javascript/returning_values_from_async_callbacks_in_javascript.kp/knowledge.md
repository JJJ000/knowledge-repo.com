---
title: What is the process for obtaining a result from an asynchronous callback function?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Return the value from the callback function by passing it as an argument to a callback function.
---

**Contents**

[TOC]

#Section 1: Overview

Asynchronous callback functions are functions that are called after the completion of an asynchronous task, such as an API call. These functions are often used to handle the response data or errors returned by the asynchronous task.

#Section 2: Return Value

The return value of an asynchronous callback function is usually the data or error returned by the asynchronous task. This data or error can be returned directly from the callback function, or it can be stored in a variable and then returned from the function.

#Section 3: Examples

Example 1:

// Function to make API call
const makeApiCall = async () => {
  // Make API call
  const response = await fetch('/api/data');
  // Return response
  return response;
};

// Asynchronous callback function
const handleApiResponse = (response) => {
  // Check if response is successful
  if (response.ok) {
    // Return response data
    return response.data;
  } else {
    // Return error
    return response.error;
  }
};

// Make API call
makeApiCall()
  .then((response) => {
    // Handle response
    const data = handleApiResponse(response);
    // Return data
    return data;
  });

Example 2:

// Function to make API call
const makeApiCall = async () => {
  // Make API call
  const response = await fetch('/api/data');
  // Return response
  return response;
};

// Asynchronous callback function
const handleApiResponse = (response) => {
  // Create variable to store response data or error
  let data;
  // Check if response is successful
  if (response.ok) {
    // Store response data
    data = response.data;
  } else {
    // Store error
    data = response.error;
  }
  // Return data or error
  return data;
};

// Make API call
makeApiCall()
  .then((response) => {
    // Handle response
    const data = handleApiResponse(response);
    // Return data
    return data;
  });
