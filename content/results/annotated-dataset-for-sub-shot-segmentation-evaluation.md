---
excerpt: 'This dataset was created for evaluating the performance of the developed motion-driven approach for fine-grained temporal segmentation of user-generated videos'
types: results
tags:
- data
images: []
layout: results
title: Annotated dataset for sub-shot segmentation evaluation
date: '2017-08-31T16:47:22+03:00'
---
<p><strong>Description</strong></p>
<p>This dataset was created for evaluating the performance of the developed motion-driven approach for fine-grained temporal segmentation of user-generated videos, that is reported in [1].</p>
<p>Given the fact that user-generated videos are most commonly captured without interruption using a single camera, thus being single-shot videos, their fine-grained temporal segmentation aims to identify visually coherent parts (called sub-shots) that correspond to individual actions taking place during the video recording, such as left camera panning, camera zoom-out or tracking of a moving object.</p>
<p>Based on the above, the created dataset contains the ground-truth sub-shot segmentation for 33 single-shot videos. This ground-truth segmentation was created by human annotation of the sub-shot boundaries for each video, where each boundary indicates the end of a visually and temporally contiguous activity of the video recording device and the start of the next one (e.g. a downward camera tilting that is followed by a camera zoom-in). Overall, our dataset contains 674 sub-shot transitions.</p>
<p>The set of videos can be divided in three parts:</p>
<ol>
	<li><em>Own Videos</em>: 15 single-shot videos of total duration 6 minutes, which contain clearly defined fragments that correspond to several video recording activities;</li>
	<li><em>Amateur Videos</em>: 5 single-shot amateur videos of total duration 17 minutes, found on the YouTube platform;</li>
	<li><em>Movie Excerpts</em>: 13 single-shot parts of known movies of total duration 46 minutes which represent professional video content.</li>
</ol>
<p>The videos of the first part were recorded in the external spaces of our (CERTH-ITI) facilities using an iPhone 5 smart-phone. These videos and their ground-truth are freely provided through the "Provided files" section below.</p>
<p>The videos of the second and third part can be found on the YouTube platform (links in the "Video collection" section below). For these videos we only provide the ground-truth data again through the "Provided files" section below.</p>
<p><strong>Video Collection</strong></p>
<p>For each video of the dataset we provide:</p>
<ul>
	<li>The video ID;</li>
	<li>The video filename for "Own videos" and the YouTube video name and URL for "Amateur videos" and "Movie Excerpts" (accessed on 12/11/2017);</li>
	<li>The video frame-rate that directly affects the ground-truth annotation; the videos of the second and third part should be downloaded at the corresponding frame-rates (default values when using the KeepVid web application -&nbsp;<a href="https://keepvid.com/">https://keepvid.com/</a>) to match the created annotations.</li>
</ul>
<p>The above information is included in a table that is available <a href="http://mklab.iti.gr/files/video_collection.pdf">here</a>.</p>
<p><strong>Provided files</strong></p>
<p>The needed files for using the created dataset can be downloaded from <a href="http://mklab.iti.gr/files/dataset.zip">here</a>. After unpacking the compressed file ("dataset.zip") a structure of directories will be generated. In this structure:</p>
<ol>
	<li>The "videos/own_videos" directory contains: a) the video files of the first part of the dataset, and b) the "list.txt" file which lists the video id, the filename and the frame-rate for each video of the "Own videos" collection, in a tab-separated format.</li>
	<li>The "videos/amateur_videos" directory contains the "list.txt" file which lists the video id, the filename and the frame-rate for each video of the "Amateur videos" collection, in a tab-separated format.</li>
	<li>The "videos/movie_excerpts" directory contains the "list.txt" file which lists the video id, the filename and the frame-rate for each video of the "Movie excerpts" collection, in a tab-separated format.</li>
	<li>The "ground_truth" directory contains 33 txt files (one per video) where each file is named after the ID of the corresponding video and includes the annotation of the sub-shots in the video; each line of this file corresponds to the starting frame of a sub-shot of the video (using a zero-based index of frames).</li>
	<li>The "evaluation" directory contains a simple Matlab script, called "eval_segm.m", that was used for evaluating the results of the sub-shot segmentation analysis.</li>
	<li>A readme file that contains the documentation of the dataset (i.e. the information that is available in this webpage).</li>
</ol>
<p><strong>Copyright</strong></p>
<p>CERTH-ITI holds the copyright of the “<em>Own videos</em>” part of the dataset. These videos can be freely used for academic/research purposes only and their public playback is not allowed. CERTH-ITI does not own the copyright of the “<em>Amateur Videos</em>” and “<em>Movie Excerpts</em>” parts of the dataset. The use of these videos must abide by the YouTube copyright policy (<a href="https://www.youtube.com/yt/about/copyright/">https://www.youtube.com/yt/about/copyright/</a>). Any users of these videos must accept full responsibility for the use of these parts of the dataset, including but not limited to the use of any copies of copyrighted videos that they may create from the dataset.</p>
<p><strong>Publication</strong></p>
<p>If you use this dataset, please cite the following scientific work:</p>
<p>[1] K. Apostolidis, E. Apostolidis, V. Mezaris, <em>"A motion-driven approach for fine-grained temporal segmentation of user-generated videos"</em>, Proc. 24th Int. Conf. on Multimedia Modeling (MMM2018), Bangkok, Thailand, Feb. 2018.</p>
<div>
	<p>Bib entry: @InProceedings{kapost_2018_MMM, author = {Apostolidis, Konstantinos and Apostolidis, Evlampios and Mezaris, Vasileios}, title = {A motion-driven approach for fine-grained temporal segmentation of user-generated videos}, booktitle = {The 24th International Conference on Multimedia Modeling (MMM)}, month = {Feb}, year = {2018}}</p>
</div>
<p><strong>Contact</strong></p>
<p>For any queries, please contact the authors of the aforementioned scientific work at: <a href="mailto:kapost@iti.gr">kapost@iti.gr</a> (K. Apostolidis), <a href="mailto:apostolid@iti.gr">apostolid@iti.gr</a> (E. Apostolidis), <a href="mailto:bmezaris@iti.gr">bmezaris@iti.gr</a> (V. Mezaris).</p>
<p><strong>Acknowledgements</strong></p>
<p>This work was supported by the EU’s Horizon 2020 research and innovation programme under grant agreement H2020-732665 EMMA.</p>
