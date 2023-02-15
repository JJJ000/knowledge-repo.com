---
title: Mysql 5.7.12 import is unable to create a JSON value from a string with the character set 'binary'
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: No, MySQL 5.7.12 cannot create a JSON value from a string with CHARACTER SET `binary` in JSON.
---

**Contents**

[TOC]

**Section 1: Overview**

MySQL 5.7.12 import cannot create a JSON value from a string with CHARACTER SET 'binary'. This is due to the fact that the JSON data type is not supported in MySQL 5.7.12.

**Section 2: Character Set 'Binary'**

The CHARACTER SET 'binary' is a type of character set that is used to denote a collection of characters that are encoded in a binary format. Binary character sets are used to represent text in a way that is more efficient than traditional character sets, such as ASCII or Unicode.

**Section 3: JSON Data Type**

The JSON data type is a data type that is used to store and manipulate JSON documents. JSON documents are used to store and exchange data between applications. The JSON data type allows applications to store and manipulate documents in a more efficient way than traditional data types.

**Section 4: Conclusion**

In conclusion, MySQL 5.7.12 import cannot create a JSON value from a string with CHARACTER SET 'binary' because the JSON data type is not supported in MySQL 5.7.12. This means that applications must use other data types to store and manipulate JSON documents.
