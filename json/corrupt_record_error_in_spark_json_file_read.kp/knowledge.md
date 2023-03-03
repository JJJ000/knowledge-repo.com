---
title: Error encountered when attempting to read a JSON file into spark due to corrupt record
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-03 00:00:00
updated_at: 2023-03-03 00:00:00
tldr: The `org.apache.spark.sql.execution.datasources.DataSource$.org$apache$spark$sql$execution$datasources$DataSource$$verifyStreamAndInferSchema` method can be used to detect and skip corrupt records when reading a JSON file into Spark.
---

**Contents**

[TOC]

### Causes

The most common cause of the `org.apache.spark.sql.AnalysisException: Malformed records are detected in record parsing. ParseToJson` error is when a JSON file contains invalid JSON records. This can happen if the JSON file contains extra characters, such as a comma at the end of a line, or if the JSON file contains a record that is not properly formatted.

### Solutions

The best way to solve this error is to use a JSON validator to check the JSON file for any errors before attempting to read it into Spark. This will help ensure that the file is properly formatted and can be read into Spark without any issues. Additionally, it is important to make sure that the JSON file is properly formatted and does not contain any extra characters. If there are any errors, it should be corrected before attempting to read the file into Spark.

### Prevention

To prevent this error from occurring in the future, it is important to make sure that any JSON files are properly formatted and validated before attempting to read them into Spark. Additionally, it is important to make sure that the JSON file does not contain any extra characters, such as a comma at the end of a line. Finally, if any errors are found, they should be corrected before attempting to read the file into Spark.
