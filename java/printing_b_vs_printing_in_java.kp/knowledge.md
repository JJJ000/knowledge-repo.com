---
title: What causes the significant difference in speed between printing "B" and printing "#"?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-23 00:00:00
updated_at: 2023-01-23 00:00:00
tldr: Printing `B` requires two bytes to be printed, while printing `#` requires only one byte, thus making `B` slower.
---

**Contents**

[TOC]

### Processing Time
Printing "B" is slower than printing "#" because it takes longer for the processor to process the character. The processor must look up the character in its memory and then send it to the printer. The processor looks up the character "#" much faster than the character "B" because the character "#" is represented by a single byte in the processor's memory, while the character "B" is represented by two bytes.

### Printer Setup
Printing "B" is also slower than printing "#" due to the printer setup. The printer must interpret the character "B" as a two-byte character, while the character "#" is interpreted as a single byte. This requires the printer to perform additional setup steps to interpret the character "B" correctly, which takes additional time.

### Printing Speed
Lastly, printing "B" is slower than printing "#" due to the speed of the printer. The printer must physically move the print head to print each character, and the print head must move faster to print the character "#" than it must move to print the character "B". This is because the character "#" is smaller and requires less movement of the print head to print it than the character "B".
