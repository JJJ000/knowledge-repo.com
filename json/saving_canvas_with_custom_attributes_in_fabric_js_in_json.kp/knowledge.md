---
title: How to use fabric.js to save a canvas on a server with custom attributes
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Fabric.js provides an API method called toJSON() which can be used to save the canvas on the server with custom attributes in JSON format.
---

**Contents**

[TOC]

#### Section 1: Setting Up the Server

Before you can save your canvas to the server, you will need to set up the server to accept the incoming data. You will need to create an endpoint to receive the data, which can be done using a server-side language like PHP, Node.js, or Python. This endpoint should be set up to accept a JSON object containing the attributes of the canvas.

#### Section 2: Serializing the Canvas

Once the server is set up, you will need to serialize the canvas in order to send it to the server. To do this, you can use the `toJSON()` method provided by Fabric.js. This method will return a JSON object containing all of the attributes of the canvas, which can then be sent to the server.

#### Section 3: Sending the Data to the Server

Once the canvas has been serialized, you can send the data to the server using an AJAX request. You will need to set up the request to send the JSON object to the endpoint you created in the first step.

#### Section 4: Storing the Data

Once the data has been received by the server, you will need to store it in a database. Depending on the server-side language you are using, you will need to use the appropriate methods to store the data in the database. Once the data is stored, it can be retrieved and used at any time.
