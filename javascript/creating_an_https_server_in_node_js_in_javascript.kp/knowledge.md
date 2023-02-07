---
title: What steps are needed to set up an https server in node.js?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: To create an HTTPS server in Node.js in Javascript, use the `https` module to create an HTTPS server with the `createServer()` method.
---

**Contents**

[TOC]

# Section 1: Setting up the Server

1. Install the `https` module: 
```
npm install https
```
2. Create a JavaScript file for the server and import the `https` module: 
```
const https = require('https');
```
3. Create an HTTPS server with the `https.createServer()` method: 
```
const server = https.createServer((req, res) => {
  // This is where your server code will go
});
```

# Section 2: Configuring the Server

1. Generate a private key and a certificate signing request (CSR): 
```
openssl req -nodes -new -x509 -keyout server.key -out server.cert
```
2. Configure the server with the `server.key` and `server.cert` files: 
```
const server = https.createServer({
  key: fs.readFileSync('server.key'),
  cert: fs.readFileSync('server.cert')
}, (req, res) => {
  // This is where your server code will go
});
```

# Section 3: Listening for Requests

1. Start the server with the `server.listen()` method: 
```
server.listen(port, () => {
  console.log(`Server listening on port ${port}`);
});
```

# Section 4: Testing the Server

1. Make an HTTPS request to the server using `curl`: 
```
curl -k https://localhost:port
```
2. If the request is successful, you should see the server's response in the terminal.
