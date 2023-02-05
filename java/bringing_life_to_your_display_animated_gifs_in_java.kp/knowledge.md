---
title: Show animated gif
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Animated GIFs can be displayed in Java using the javax.swing.ImageIcon class.
---

**Contents**

[TOC]

##### Using ImageIcon

One way to display an animated GIF in Java is to use an ImageIcon. An ImageIcon is an implementation of the Icon interface that paints icon-sized images. It is a lightweight component that can be used to display an image from a file or from a URL.

To display an animated GIF, create an ImageIcon object and pass the path or URL of the animated GIF as a parameter. This will create an ImageIcon object that contains the animation.

Once the ImageIcon object has been created, it can be used to display the animation on a JLabel or any other Swing component. To do this, simply call the setIcon() method of the component, passing in the ImageIcon object as a parameter.

##### Using ImageIO

Another way to display an animated GIF in Java is to use the ImageIO class. The ImageIO class provides a static read() method that can be used to read an image from a file or from a URL.

To display an animated GIF, simply call the ImageIO.read() method and pass the path or URL of the animated GIF as a parameter. This will return an Image object that contains the animation.

Once the Image object has been created, it can be used to display the animation on a JLabel or any other Swing component. To do this, simply call the setIcon() method of the component, passing in the Image object as a parameter.

##### Using ImageIcon and ImageIO Together

It is also possible to combine the use of ImageIcon and ImageIO to display an animated GIF in Java. To do this, first create an ImageIcon object and pass the path or URL of the animated GIF as a parameter. This will create an ImageIcon object that contains the animation.

Next, call the ImageIO.read() method and pass the path or URL of the animated GIF as a parameter. This will return an Image object that contains the animation.

Finally, call the setIcon() method of the component, passing in the ImageIcon object and the Image object as parameters. This will set the animation on the component.
