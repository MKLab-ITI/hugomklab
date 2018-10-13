---
excerpt: 'A tool for automatic temporal segmentation of videos into shots and scenes'
types: results
aliases:
- /results/shot-scene-segmentation
tags:
- tool
images: []
layout: results
title: Video Shot and Scene Segmentation
date: '2014-05-05T20:21:58+03:00'
---
<p><strong>Description </strong></p>
<p>This is a tool for automatic temporal segmentation of videos into shots and scenes. Shots are sequences of consecutive frames captured without interruption by a single camera. The transition between two successive shots of the video can be abrupt, where one frame belongs to a shot and the following frame belongs to the next shot, or gradual, where, two shots are combined using chromatic, spatial or spatial-chromatic video production effects (e.g., fade in/out, dissolve, wipe), which gradually replace one shot by another. This tool is capable of detecting both types of transitions. Scenes are higher level temporal fragments that correspond to the story-telling parts of the video. They are formed by grouping the detected shots into semantically coherent temporal video fragments. Parallel computing, either CPU-based (via multi-threading) or GPU-based (via CUDA programming), is used, depending on the version of the tool,&nbsp;for making the whole video analysis several times faster than real-time processing.</p>
<p><strong>Usage</strong></p>
<ol>
	<li>Download the appropriate <strong>tar.gz </strong>from the list below.</li>
	<li>Unpack the <strong>tar.gz </strong>archive creating a new folder.</li>
	<li>Run the software&nbsp;following the instructions in the included "documentation.pdf" file.</li>
</ol>
<p><strong>Output</strong></p>
<p>After the processing is finished, the folder where the analyzed video is placed, will contain four newly created results files:</p>
<ul>
	<li>The file&nbsp;<strong>"&lt;video_name&gt;_shots.txt"&nbsp;</strong>contains information about the automatically detected shots (following lines of the document). For each shot the software stores a new line with information about the starting and ending frames of the shot, plus three intermediate frames that can be used as representative keyframes of this shot in other visual analysis tasks (e.g., for video concept detection and video event detection)</li>
	<li>The file&nbsp;<strong>"&lt;video_name&gt;_shots.srt"&nbsp;</strong>contains the automatically detected shots in the format of video's subtitles, enabling the user to check visually the produced output (after renaming the file as the name of the video, and using e.g. the VLC player, or other players)</li>
	<li>The file&nbsp;<strong>"&lt;video_name&gt;_scenes.txt"</strong><strong>&nbsp;</strong>contains information about the automatically detected scenes. For each scene the software stores a new line with seven (7) numbers. The first two frames represent the starting and ending frames of the shot, while the next five numbers are the five most representative keyframes of the scene. If the last two numbers of a scene are zero this means that the scene consists of only one shot, thus we list only three keyframes.</li>
	<li value="4">The file&nbsp;<strong>"&lt;video_name&gt;_scenes.srt"&nbsp;</strong>contains the automatically detected scenes in the format of video's subtitles, enabling the user to check visually the produced output (after renaming the file as the name of the video, and using e.g. the VLC player, or other players)</li>
</ul>
<p><strong>Prerequisites (only for the GPU-based versions of the tool)</strong></p>
<ul>
	<li>NVIDIA graphics card that supports CUDA technology with the latest drivers installed</li>
	<li>CUDA Toolkit version 5.5 installed (<a href="https://developer.nvidia.com/cuda-toolkit-55-archive">https://developer.nvidia.com/cuda-toolkit-55-archive</a>)</li>
</ul>
<p><strong>Limitations </strong></p>
<p>This free version of the software can process videos of duration up to 10 minutes each. For obtaining an unrestricted version, please contact us at: <a href="mailto:shotsegmentation@iti.gr">shotsegmentation@iti.gr</a></p>
<p>The software was tested, in terms of compatibility, using various video formats and codecs, including MPEG, MP4, AVI, WMV, MOV, WEBM, FLV, and to our knowledge all other video formats and codecs supported by FFmpeg can also be processed. However, if a problem with another type of video occurs, please contact us at: <a href="mailto:shotsegmentation@iti.gr">shotsegmentation@iti.gr</a></p>
<p><strong>Version history</strong></p>
<p><strong>Version 1.0 (Released 02/05/2014)</strong></p>
<p>This release is based on the OpenCV library version 2.4.7 and the CUDA Toolkit version 5.5. It performs only segmentation to shots. The ORB descriptor and HSV histograms are used for the representation of the visual content. The detection of shot transitions is performed by assessing the visual similarity between successive on non-successive video frames. False alarms are filtered out by exploiting motion information and a flashlight detector. Version 1.0 has been replaced by the newer version 1.1.</p>
<p><strong>Version 1.1 (Released 30/05/2014)</strong></p>
<p>This release is based on the OpenCV library version 2.4.7 and the CUDA Toolkit version 5.5. It performs only segmentation to shots. It offers improved performance regarding the detection of gradual transitions, substituting the use of motion information by two gradual transition detectors. The first one detects wipe transitions. The second one detects dissolve and fade in/out transitions. Version 1.1 has been replaced by the newer version 1.2.</p>
<p><strong>Version 1.2 (Released 24/06/2014)</strong></p>
<p>This release is based on the OpenCV library version 2.4.7 and the CUDA Toolkit version 5.5. It extends the previous version by integrating algorithms for video scene segmentation and keyframe selection (up to 5 most representative keyframes of each scene are identified), on top of the shot segmentation. The new additions do not affect the processing speed, which remains at least 2 times faster than real-time processing (depending on the processing capability of the graphics card) for the entire video analysis chain (i.e., shot segmentation, scene segmentation and keyframe selection).&nbsp;Version 1.2 has been replaced by the newer version 1.3.</p>
<p><strong>Version 1.3 (Released 19/08/2014)</strong></p>
<p>This release is based on the OpenCV library version 2.4.7. It uses exclusively CPU-based processing, while the analysis is accelerated by invoking multi-threading / multi-processing operations of the Intel OpenMP runtime library.&nbsp;This release is about 7 times faster than real-time processing, on an Intel i7 PC.</p>
<p><strong>Version 1.4 (Released 09/09/2014)</strong></p>
<p>This release is the same as version 1.3, but shipped with runtime libraries of smaller size, resulting in a much more compact software package.</p>
<p><strong>Version 1.4.1 (Released 26/11/2014)</strong></p>
<p>This release is an update of version 1.4, after fixing a number of bugs.</p>
<p><strong>Version 1.4.2 (Released 29/07/2015)</strong></p>
<p>This release is an update of version 1.4.1, after utilizing a newer version of the OpenCV library (ver. 2.4.9), shipping it with a much smaller number of runtime libraries&nbsp;and fixing a few bugs.</p>
<p><strong>Version 1.4.3 (Released 05/08/2016)</strong></p>
<p>This release is a compatibility update of version 1.4.2 in order to run on Win10 and Ubuntu 14 and 16 releases, while a few minor bug fixes have been made.</p>
<p><strong>Version 1.4.4 (Released 10/04/2017)</strong></p>
<p>This release introduces four optional arguments in the software's argument list, that enable i) to run shot segmentation only, instead of both shot and scene segmentation, ii) to include in the output results files information about the type of each detected shot transition (abrupt, dissolve, wipe), iii) to choose the output path of the extracted keyframes, and iv) to choose the number of extracted keyframes per shot.</p>
<p><strong>Version 1.4.5 (Released 27/04/2018)</strong></p>
<p>This release is an update of version 1.4.4 with some bug fixes</p>
<p><u>Note:</u>&nbsp;in recent tests on a PC having Windows 7, Intel Core i7-2600K @ 3.40 GHz, 8GB RAM, and an NVIDIA GeForce GTX 560, our latest CPU version (v1.4.x found under "Latest Edition" bellow) took about 13,5% of the run-time duration of the video to complete its processing (i.e., for a 10-min 480x360 video the processing took about 1 min 20 sec), with the GPU version (found under "Other compatibility options" bellow) took about 32,5%. It is therefore suggested that you use the CPU version bellow (v1.4.x), or you may also want to try the GPU version if your GPU hardware is significantly better than that of our test PC.</p>
<p><strong>Downloads</strong></p>
<p>Latest Edition (v.1.4.5)</p>
<ul>
	<li><a href="http://mklab.iti.gr/files/Windows 64-bit v1.4.5.zip">Windows 64-bit v1.4.5.zip</a> <strong>(CPU-version&nbsp;1.4.5) /&nbsp;Compatible with: 64-bit installations&nbsp;of&nbsp;Windows (XP, Vista, Win7, Win8/8.1, Win10)</strong></li>
	<li><a href="http://mklab.iti.gr/files/Ubuntu 16.04 64-bit v1.4.5.tar.gz">Ubuntu 16.04 64-bit&nbsp;v1.4.5.tar.gz</a>&nbsp;<strong>(CPU-version 1.4.5)&nbsp;/&nbsp;<strong>Compatible with: 64</strong><strong>-bit installations&nbsp;of Ubuntu 16.04</strong></strong></li>
</ul>
<p>Previous Editions</p>
<ul>
	<li><a href="http://mklab.iti.gr/files/Windows 64-bit v1.4.4.tar.gz">Windows 64-bit v1.4.4.tar.gz</a>&nbsp;<strong>(CPU-version&nbsp;1.4.4) /&nbsp;Compatible with: 64-bit installations&nbsp;of&nbsp;Windows (XP, Vista, Win7, Win8/8.1, Win10)</strong></li>
	<li><a href="http://mklab.iti.gr/files/Ubuntu 16.04 64-bit v1.4.4.tar.gz">Ubuntu 16.04 64-bit&nbsp;v1.4.4.tar.gz</a>&nbsp;<strong>(CPU-version 1.4.4)&nbsp;/&nbsp;<strong>Compatible with: 64</strong><strong>-bit installations&nbsp;of Ubuntu 16.04</strong></strong></li>
</ul>
<ul>
	<li><a href="http://mklab.iti.gr/files/Windows 32-bit v1.4.3.tar.gz">Windows 32-bit v1.4.3.tar.gz</a>&nbsp;<strong>(CPU-version&nbsp;1.4.3) /&nbsp;Compatible with: 32</strong><strong>-bit installations&nbsp;of&nbsp;Windows&nbsp;</strong><strong>(XP,&nbsp;Vista, Win7,&nbsp;Win8/8.1, Win10)</strong></li>
	<li><a href="http://mklab.iti.gr/files/Ubuntu 14.04 64-bit v1.4.3.tar.gz">Ubuntu 14.04 64-bit&nbsp;v1.4.3.tar.gz</a>&nbsp;<strong>(CPU-version 1.4.3)&nbsp;/&nbsp;<strong>Compatible with: 64</strong><strong>-bit installations&nbsp;of <strong><strong>Ubuntu 14.04</strong></strong></strong></strong></li>
</ul>
<p>Other compatibility options</p>
<ul>
	<li><a href="http://mklab.iti.gr/files/Windows 64-bit v1.2.tar.gz">Windows 64-bit v1.2.tar.gz</a>&nbsp;<strong>(GPU-version&nbsp;1.2) /&nbsp;Compatible with: Windows 7, Windows&nbsp;8, and some Windows XP and Windows Vista installations with multi-threading support (Intel TBB library)</strong></li>
	<li><a href="http://mklab.iti.gr/files/Windows 32-bit tbb v1.2.tar.gz">Windows 32-bit tbb v1.2.tar.gz</a>&nbsp;<strong>(GPU-version&nbsp;1.2) /&nbsp;Compatible with: Windows 7, Windows&nbsp;8, and some Windows XP and Windows Vista installations&nbsp;with multi-threading support (Intel TBB library)</strong></li>
	<li><a href="http://mklab.iti.gr/files/Windows 32-bit NOtbb v1.2.tar.gz">Windows 32-bit NOtbb v1.2.tar.gz</a>&nbsp;<strong>(GPU-version&nbsp;1.2) /&nbsp;Compatible with: Windows XP&nbsp;and Windows Vista installations without multi-threading support</strong></li>
</ul>
<p><strong>Publication </strong></p>
<p>This software is based exclusively on free-to-use and non-patented modules of the OpenCV library, and implements variations of the shot segmentation and scene segmentation algorithms introduced in the following publications [1] and [2] (please cite these papers if you use the provided software):</p>
<p><em>[1] E. Apostolidis, V. Mezaris, "Fast Shot Segmentation Combining Global and Local Visual Descriptors", Proceedings of IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), Florence, Italy, May 2014.</em></p>
<p><em>[2] P. Sidiropoulos, V. Mezaris, I. Kompatsiaris, H. Meinedo, M. Bugalho, I. Trancoso, "Temporal video segmentation to scenes using high-level audiovisual features", IEEE Transactions on Circuits and Systems for Video Technology, vol. 21, no. 8, pp. 1163-1177, August 2011.</em></p>
<p><strong>License </strong></p>
<p>Copyright (C) 2014 Vasileios Mezaris, Evlampios Apostolidis, Alexandros Pournaras / CERTH-ITI. All Rights Reserved.</p>
<p>Redistribution and use in binary form, without modification, is permitted provided that the following conditions are met:</p>
<ol>
	<li>Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.</li>
	<li>The name of the author may not be used to endorse or promote products derived from this software without specific prior written permission.</li>
</ol>
<p>This software is provided by the authors "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. In no event shall the authors be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.</p>
<p>The implementation of certain components used by this software was based on the OpenCV library. Below is the original copyright.</p>
<p align="center">License Agreement</p>
<p align="center">For Open Source Computer Vision Library</p>
<p align="center">Copyright (C) 2000-2008, Intel Corporation, all rights reserved.</p>
<p align="center">Copyright (C) 2008-2011, Willow Garage Inc., all rights reserved.</p>
<p align="center">Third party copyrights are property of their respective owners.</p>
<p>Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:</p>
<p>* Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.</p>
<p>* Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.</p>
<p>* The name of the copyright holders may not be used to endorse or promote product derived from this software without specific prior written permission.</p>
<p>This software is provided by the copyright holders and contributors "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. In no event shall the Intel Corporation or contributors be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.</p>
<p>The implementation of certain components used by some versions of this software was based on the Intel OpenMP runtime library. Below is the original copyright.</p>
<div style="text-align: center;">Copyright (c) 2013, Intel Corporation</div>
<div style="text-align: center;">&nbsp;</div>
<div style="text-align: center;">All rights reserved.</div>
<div style="text-align: center;">&nbsp;</div>
<div>
	<p>Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:</p>
	<p>* Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.</p>
	<p>* Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.</p>
	<p>* Neither the name of Intel Corporation nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.</p>
</div>
<div>This software is provided by the copyright holders and contributors "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. In no event shall the copyright holder or contributors be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.</div>
<div>&nbsp;</div>
<p><strong>Acknowledgements</strong></p>
<p>This work was supported in part by the European Commission under contracts FP7-287911 LinkedTV and FP7-318101 MediaMixer.</p>
<p><strong>Contacts </strong></p>
<p>You may contact the software developing team (Vasileios Mezaris, Evlampios Apostolidis and Alexandros Pournaras) by sending e-mail at <a href="mailto:shotsegmentation@iti.gr">shotsegmentation@iti.gr</a> for any question or remark you may have with respect to this tool.</p>
