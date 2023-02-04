---
title: Transform a string into title case using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the .toUpperCase() and .toLowerCase() methods on the string, as well as the .replace() method to convert a string to Title Case.
---

**Contents**

[TOC]

**Section 1: Understanding Title Case**

Title Case is a style of capitalization that is commonly used for titles, headings, and other proper nouns. It involves capitalizing the first letter of each word in a phrase, with the exception of certain words such as prepositions, articles, and conjunctions.

**Section 2: Using JavaScript to Convert to Title Case**

JavaScript provides a built-in method, `toUpperCase()`, which can be used to convert a string to Title Case. The `toUpperCase()` method takes a string as an argument and returns a new string with the first letter of each word capitalized.

**Section 3: Creating an Exclusion List**

In order to ensure that the words that should remain lowercase are not capitalized, it is necessary to create an exclusion list. This list should include any words that should not be capitalized, such as prepositions, articles, and conjunctions.

**Section 4: Putting it All Together**

Once the exclusion list is created, the string can be converted to Title Case by looping through each word in the string and capitalizing the first letter of each word, unless it is in the exclusion list. This can be done using a `for` loop and an `if` statement.
