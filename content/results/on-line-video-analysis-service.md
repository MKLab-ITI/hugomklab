---
title: "On Line Video Analysis Service"
date: 2018-08-30T14:39:46+03:00
excerpt: 'This experimental service lets you submit videos in various formats and perform visual analysis algorithms on them: shot segmentation, scene segmentation and visual concept detection'
types: results
tags:
- demo
layout: results
---
The service allows the user to submit a video for analysis by uploading a local copy of it from the user's machine (this is preferable), or by specifying the URL of a video available on-line. The supported on-line video sources include YouTube, DailyMotion, Facebook and Twitter (beware though that not all videos from these platforms are accessible to our service, due to platform-specific or user-defined restrictions about the use of each specific video; and, the provided URL should always point to a single video, rather than a playlist of videos). 

The service can handle videos of mp4, webm, avi, mov, wmv, ogv, mpg, flv, and mkv format. After fetching the video file, the service decomposes the video into shots and scenes. Following, a few hundred visual concept detectors are evaluated for each video shot, thus generating shot-level concept-based annotations. The complete service runs at high speed (i.e., it is several times faster than real-time video processing, on an Intel i7 PC - though delays may be noticed if multiple video processing jobs are in the queue). After submitting a video for analysis, the user may close the browser window and be notified by email when the analysis results are ready; alternatively, the user may leave the browser window open, to see how the analysis progresses. In any case, when the analysis is completed an email is sent containing the unique address at which the analysis results are displayed; the display is performed with the help of an interactive user interface, which allows the exploration of the video structure (shots, scenes) and the annotations, and the concept-based search within the collection of shots.

[Learn more](http://multimedia2.iti.gr/onlinevideoanalysis/service/start.html)