---
title: Transforming dynamodb data into standard JSON format using aws lambda
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: AWS Lambda can be used to convert DynamoDB data to normal JSON using the DynamoDB.Converter.unmarshall() function.
---

**Contents**

[TOC]

# Section 1 - Retrieve Data from DynamoDB

In order to format DynamoDB data to normal JSON in AWS Lambda, the first step is to retrieve the data from the DynamoDB table. This can be done using the DynamoDB API's `getItem` method, which can be called from within a Lambda function. The `getItem` method takes the table name and a key as parameters, and returns the item associated with that key.

# Section 2 - Convert Data to JSON

The next step is to convert the DynamoDB data to normal JSON. This can be done using the `JSON.stringify` method, which takes a JavaScript object as a parameter and returns a JSON string. The `getItem` method returns a JavaScript object, so it can be passed directly to the `JSON.stringify` method.

# Section 3 - Return JSON

Once the DynamoDB data has been converted to normal JSON, it can be returned from the Lambda function. This can be done by using the `context.succeed` method, which takes a JSON string as a parameter and returns it as the result of the Lambda function.

# Section 4 - Error Handling

Finally, it is important to consider error handling. If the `getItem` method fails to retrieve the item from the table, or if the `JSON.stringify` method fails to convert the data to JSON, then an error should be returned. This can be done by using the `context.fail` method, which takes an error message as a parameter and returns it as the result of the Lambda function.
