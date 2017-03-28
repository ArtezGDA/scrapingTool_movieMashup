# InstantTrailer
Tool for creating your instant trailer.

# Synopsis
InstantTrailer is a tool that creates new trailers based on existing ones.
It cuts scraped clips into small parts and merges them back together.


To use this tool we provide you with an existing database of videoclips, from where you can decide which ones you want to use.


# Installation
To achieve the Instant Trailer, the following steps need to happen:


--> choose scraped footage from YouTube

--> cut the footage into parts

--> merge the parts into a new trailer


Our tool would provide the last two steps. You are able to choose your own set of trailers out of the database that we provide. From here on, you should be able to cut the footage into parts and later merge the parts into a new trailer, with code that we provide. You can find all our code examples in the file 'CodeResearch'. 


Do you like to know how to scrape video's from YouTube? --> Research.md


It is very convenient to have the software project FFmpeg on your computer already. As a command line tool you can let ffmpeg edit video files in many different ways, like for example:
1. Cut video file into a smaller clip
2. Split a video into multiple parts
3. Convert video from one format to another
4. Join (concatenate) video files
5. Mute a video (Remove the audio component)
6. Extract the audio from video

And much more.


How to get your hands on FFmpeg, is explained in the 'Research.md' file. Here you can also find some convenient commands to help you out. 


# Screenshots
Screenshots of the InstantTrailer

<a href="http://nl.tinypic.com?ref=16c15bd" target="_blank"><img src="http://i63.tinypic.com/16c15bd.png" border="0" alt="Image and video hosting by TinyPic"></a>

<a href="http://nl.tinypic.com?ref=1177fcw" target="_blank"><img src="http://i68.tinypic.com/1177fcw.png" border="0" alt="Image and video hosting by TinyPic"></a>


# Examples


Here a short diagram on how the InstantTrailer works:

<a href="http://nl.tinypic.com?ref=6rht9z" target="_blank"><img src="http://i65.tinypic.com/6rht9z.jpg" border="0" alt="Diagram"></a>

A more detailed description:

### 1
First, data is collected from YouTube. This means every trailer we could find, downloaded by 4K Video Downloader.
### 2
The downloaded data (trailers) are now being put in a database, where we can work from.
### 3
Data from the database can now be imported to be cutted into small pieces. The length of an average trailer is about 2 minutes and 30 seconds (more info on the trailer --> Research.md). The small pieces therefore will have to be about 15 seconds to create a new trailer (based on the 11 steps that an average trailer follows --> Research.md). 
### 4
The footage will now be cut into pieces.
### 5
The cut footage now needs to be imported to be merged together again. The small parts from different trailers will be merged together in an order that follows the 11 steps. This will create a new trailer. 
### 6 
The cut footage will now be merged into a new trailer. 
### 7
Your endresult! A new trailer is created. 


# Motivation
As Graphic Designers we wanted to develop our own skills and learn how to build our own tools. This way we can create applications or tools that suit our own specific workflow, in contrary to what most existing applications do: they're designed for a huge audience and therefore are made for the average user. This average user doesn't necessarily have to be you. That's why it's very convenient for a designer to be able to make their own tools that optimize their own specific workflow. 
That's why we decided to make this MovieMashup tool. 

Experimenting with cutting video clips and combining them is something that has already been done by a lot of people, but we're looking for a way to make this a whole lot easier and more interesting. 
We were fascinated by the way movies and movietrailers are built up: they all seem to have the same buildup, consisting of about 8 parts. This tool can be seen as a way to ridicule the hollywood industry and at the same time create interesting video mashups.

# License 
MIT License

Copyright (c) 2017 Graphic Design Arnhem at ArtEZ Academy

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
