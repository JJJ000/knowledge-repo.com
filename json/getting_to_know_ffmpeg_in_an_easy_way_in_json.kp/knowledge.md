---
title: Find out about ffmpeg in an easy-to-understand way
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: FFmpeg information can be obtained in a friendly way in JSON format using the ffprobe command.
---

**Contents**

[TOC]

**Section 1: How to Use FFmpeg**

FFmpeg is a free, open-source command-line tool for manipulating and converting audio and video files. It supports a wide range of formats and can be used to convert between different formats, extract audio from video, and more. To use FFmpeg, you will need to open a command-line terminal and type in the appropriate commands. 

**Section 2: FFmpeg Commands**

FFmpeg supports a wide range of commands for manipulating and converting audio and video files. Some of the most common commands include: 

- `ffmpeg -i <input_file> <output_file>`: This command is used to convert an input file into an output file. 

- `ffmpeg -i <input_file> -acodec <codec> <output_file>`: This command is used to convert an input file into an output file using a specific audio codec. 

- `ffmpeg -i <input_file> -vcodec <codec> <output_file>`: This command is used to convert an input file into an output file using a specific video codec. 

- `ffmpeg -i <input_file> -ss <start_time> -t <duration> <output_file>`: This command is used to extract a portion of an input file and convert it into an output file. 

**Section 3: FFmpeg Output Formats**

FFmpeg supports a wide range of output formats, including MP4, AVI, MPEG, FLV, MOV, and more. 

**Section 4: FFmpeg in JSON Format**

FFmpeg can be used to output information in JSON format. For example, the following command will output information about an input file in JSON format: 

`ffmpeg -i <input_file> -f json -pretty`
