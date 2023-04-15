---
title: Using nodejs, add a new item to a JSON array in dynamodb
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the DocumentClient`s update function with the append operator and set the JSON Array attribute with the updated array as the expression value.
---

**Contents**

[TOC]

# Introduction 

In this tutorial, we will discuss how to append a new object to a JSON array in DynamoDB using NodeJS. DynamoDB provides a powerful document data model that permits nested attributes within records. JSON is a lightweight data interchange format that is easy for humans to read and write, and easy for machines to parse and generate. We will use these two technologies to achieve our goal.

# Steps to Append a new Object to a JSON Array in DynamoDB using NodeJS

## Step 1 - Create a DynamoDB Client

The first step is to create a client to interact with DynamoDB. We will use the `aws-sdk` library to create the client. You need to provide your `accessKeyId`, `secretAccessKey` and `region` to the client.

```javascript
const AWS = require("aws-sdk");
const dynamoDbClient = new AWS.DynamoDB.DocumentClient({
  region: "us-west-2",
  accessKeyId: "<ACCESS_KEY_ID>",
  secretAccessKey: "<SECRET_ACCESS_KEY>",
});
```

## Step 2 - Fetch the Existing JSON Array

Before we append a new object to the JSON array, we need to fetch the existing JSON array. We will read the existing JSON array from DynamoDB and store it in a variable.

```javascript
const fetchExistingArrayParams = {
  TableName: "myDynamoDBTable",
  Key: {
    id: "myRecordId",
  },
  ProjectionExpression: "myJsonArray",
};

let existingJsonArray = [];
dynamoDbClient.get(fetchExistingArrayParams, (error, data) => {
  if (error) {
    console.log(error);
  } else {
    existingJsonArray = data.Item.myJsonArray || [];
    console.log(`existing json array: ${JSON.stringify(existingJsonArray)}`);
  }
});
```

## Step 3 - Append the New Object to the Existing Array

After we have fetched the existing JSON array, we can append the new object to the existing array.

```javascript
const newObject = {
  name: "newObjectName",
  value: "newObjectValue",
};

existingJsonArray.push(newObject);

console.log(`updated json array: ${JSON.stringify(existingJsonArray)}`);
```

## Step 4 - Update the DynamoDB Record

The final step is to update the DynamoDB record with the updated JSON array. We will use the `update` method of the `dynamoDbClient` object to achieve this.

```javascript
const updateParams = {
  TableName: "myDynamoDBTable",
  Key: {
    id: "myRecordId",
  },
  UpdateExpression: "set #ja = :a",
  ExpressionAttributeNames: {
    "#ja": "myJsonArray",
  },
  ExpressionAttributeValues: {
    ":a": existingJsonArray,
  },
};

dynamoDbClient.update(updateParams, (error, data) => {
  if (error) {
    console.log(error);
  } else {
    console.log(`updated dynamodb record: ${JSON.stringify(data)}`);
  }
});
```

# Conclusion

In this tutorial, we have discussed how to append a new object to a JSON array in DynamoDB using NodeJS. We created a DynamoDB client, fetched the existing JSON array, appended a new object to the array, and updated the DynamoDB record with the updated JSON array. This is a basic example, and you can adjust it to suit your specific use case.
