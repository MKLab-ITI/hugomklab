---
excerpt: 'This work focuses on extracting binary masks that indicate which pixels in a video are active by statistical processing of inter-frame illumination variations'
types: results
tags:
- demo
images: []
layout: results
title: Activity Areas from kurtosis-based processing
date: '2009-01-14T11:37:26+02:00'
---
<p>
<strong> Videos of Human Activities inside their corresponding activity areas:</strong> 
</p>
<p>
The successful analysis of videos is often based on the information contained in the motion taking place in it. This work focuses on extracting binary masks that indicate which pixels in a video are active by statistical processing of inter-frame illumination variations. The active frame pixels are separated from static ones by detecting outliers in the inter-frame illumination variations. Outliers in the data set are detected by the application of higher order statistics, and specifically the <strong>kurtosis</strong>. Static pixels have very low kurtosis values, whereas the kurtosis of active pixels is very high. This results in the <strong>Activity Area</strong>, i.e. a binary mask that accurately localizes the active pixels in the video frames. 
</p>
<p>
The knowledge included in the activity area can be used to isolate the active pixels in a video, so as to process only those. This increases the video processing accuracy, while at the same time reducing its computational cost. For example, in [1], [2] colors in the activity area is compared with colors in the background in order to achieve moving object segmentation. In [3], [4], active pixels are further processed to detect times of change in activities. 
</p>
The videos that follow show human motions inside their corresponding Activity Areas. It is obvious that the Activity Areas capture the pixel activity with accuracy. Details such as the motion of the person's head going up and down are captured in the top of the activity areas. Similarly, other details such as small pixel areas where the person's leg is moving (e.g. on the right side of Daria Running and Moshe Running) are captured.<br />
<br />
<p>
<em><strong>Click on the thumbnails below to see the person moving inside the Activity Area. 
</strong></em>
</p>
<table border="0" cellspacing="2" cellpadding="4" align="center">
	<tbody>
		<tr>
			<td>
			<p>
			Daria Running  
			</p>
			<p>
			<a href="/files/demos/harec/daria_run_AA_video.mpg"><img src="/files/demos/harec/daria_run_AA_video.mpg.jpg" alt="" width="160" height="120" /></a>
			</p>
			</td>
			<td>
			<p>
			Moshe Running  
			</p>
			<p>
			<a href="/files/demos/harec/moshe_run_AA_video.mpg"><img src="/files/demos/harec/moshe_run_AA_video.mpg.jpg" alt="" width="160" height="120" /></a>
			</p>
			</td>
			<td>
			<p>
			Daria Jumping 
			</p>
			<p>
			<a href="/files/demos/harec/daria_jump_AA_video.mpg"><img src="/files/demos/harec/daria_jump_AA_video.mpg.jpg" alt="" width="160" height="120" /></a>
			</p>
			</td>
		</tr>
		<tr>
			<td>
			<p>
			Lena Jumping 
			</p>
			<p>
			<a href="/files/demos/harec/lena_jump_AA_video.mpg"><img src="/files/demos/harec/lena_jump_AA_video.mpg.jpg" alt="" width="160" height="120" /></a>
			</p>
			</td>
			<td colspan="2">
			<p>
			Shahar Jumping in place
			</p>
			<p>
			<a href="/files/demos/harec/shahar_pjump_AA_video.mpg"><img src="/files/demos/harec/shahar_pjump_AA_video.mpg.jpg" alt="" width="160" height="120" /></a>
			</p>
			</td>
		</tr>
	</tbody>
</table>
<p>
<strong>References:</strong> 
</p>
<p>
[1] A. Briassouli, V. Mezaris, I. Kompatsiaris, &quot;Color
aided motion-segmentation and object tracking for video sequences
semantic analysis&quot;, <a href="http://www3.interscience.wiley.com/cgi-bin/jhome/37666?CRETRY=1&amp;SRETRY=0" target="_blank">International Journal of Imaging Systems and Technology (IJIST)</a>, Special Issue on Applied Color Image Processing, Volume 17, Issue 3, pp 174-189, 2007.<a href="/files/pdf/IMA.pdf"><img src="/files/pdf/pdf.png" border="0" alt="" align="top" /></a>
</p>
<p>
[2] A. Briassouli, V. Mezaris, I. Kompatsiaris, &quot;Combination of Accumulated
Motion and Color Segmentation for Human Activity Analysis&quot;, EURASIP
Journal on Image and Video Processing, vol. 2008, Article ID 735141,
2008.<a href="/files/pdf/humancentric_final.pdf"><img src="/files/pdf/pdf.png" border="0" alt="" align="top" /></a> 
</p>
<p>
[3] A. Briassouli, I. Kompatsiaris, &quot;Statistical Processing of
Video for Detection of Events in Space and Time&quot;, IEEE International
Conference on Multimedia and Expo (ICME), June 23-26, 2008, Hannover,
Germany.
<a href="/files/pdf/video_stats_event.pdf"><img src="/files/pdf/pdf.png" border="0" alt="" align="top" /></a>
</p>
<p>
[4] Alexia Briassouli, Ioannis Kompatsiaris, &quot;Human Activity Localization
via Sequential Change Detection&quot;, ACM Multimedia-MIR 2008, Oct 27-31
2008, Vancouver, Canada.<a href="/files/pdf/Seq_Det_Surv.pdf"><img src="/files/pdf/pdf.png" border="0" alt="" align="top" /></a>
</p>
<p>
&nbsp;
</p>
