---
title: Creating audio effects using JavaScript and html5
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: JavaScript and HTML5 can be used to create sound effects using the Audio API and the Web Audio API.
---

**Contents**

[TOC]

## Using HTML5 Audio
HTML5 Audio provides an easy way to include sound effects in your web page. To use HTML5 Audio, you simply need to add the `<audio>` tag to your HTML document and specify the source of the audio file.

```
<audio src="sound.mp3" controls>
  Your browser does not support the <code>audio</code> element.
</audio>
```

You can also customize the audio playback with attributes such as `autoplay` and `loop`.

## Using JavaScript
You can also use JavaScript to create and control sound effects. The Web Audio API provides an interface for controlling audio on the web. It includes methods for creating sound sources, manipulating audio, and controlling playback.

For example, the following code creates an oscillator and plays a sound at a given frequency:

```
var context = new AudioContext();
var oscillator = context.createOscillator();
oscillator.frequency.value = 440;
oscillator.start();
```

You can also use the Web Audio API to create more complex sound effects. For example, you can use the `createBufferSource()` method to create a sound buffer and play it back with the `start()` method.

## Using Libraries
There are also several JavaScript libraries that make it easier to create and control sound effects. For example, the Howler.js library provides an easy-to-use API for creating and controlling sound effects.

For example, the following code creates a sound and plays it back:

```
var sound = new Howl({
  src: ['sound.mp3']
});

sound.play();
```

The library also includes methods for controlling the playback, such as `pause()`, `stop()`, and `fade()`.
