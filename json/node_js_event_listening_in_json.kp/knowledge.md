---
title: Hear all events broadcasted in node.js
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can listen to all emitted events in Node.js by using the `JSON.stringify()` method.
---

**Contents**

[TOC]

**Section 1: Setting Up the Event Emitter**

The first step to listening to all emitted events in Node.js is to set up the Event Emitter. This is done by using the `require()` function to import the `events` package from the Node.js core library.

```javascript
const EventEmitter = require('events');
```

**Section 2: Creating an Event Emitter Instance**

After importing the `events` package, the next step is to create an instance of the Event Emitter. This is done by creating a new instance of the `EventEmitter` class.

```javascript
const emitter = new EventEmitter();
```

**Section 3: Listening for Events**

Once the Event Emitter instance is created, the next step is to listen for events. This is done by using the `on()` method of the Event Emitter instance. This method takes two parameters: the event name and the callback function.

```javascript
emitter.on('myEvent', (data) => {
  console.log(data);
});
```

**Section 4: Emitting Events**

The final step is to emit the events. This is done by using the `emit()` method of the Event Emitter instance. This method takes two parameters: the event name and the data to be passed to the callback function.

```javascript
emitter.emit('myEvent', { message: 'Hello World!' });
```

When the event is emitted, the callback function will be called and the data passed to it will be logged to the console.
