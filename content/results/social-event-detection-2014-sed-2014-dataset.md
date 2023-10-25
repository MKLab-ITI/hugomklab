---
excerpt: 'Dataset, challenge definitions, ground truth challenge results and corresponding evaluation script that were created and used in the 2014 edition of the Social Event Detection (SED) task of the MediaEval benchmarking activity'
types: results
aliases:
- /results/sed2014
tags:
- data
- image set
images: []
layout: results
title: Social Event Detection 2014 (SED 2014) dataset
date: '2014-11-14T15:47:44+03:00'
---
<div><strong>Overview</strong>: This page makes available for research purposes the dataset, challenge definitions, ground truth challenge results and corresponding evaluation script that were created and used in the 2014 edition of the Social Event Detection (SED) task of the MediaEval benchmarking activity.</div>
<div>&nbsp;</div>
<div>The Social Event Detection (SED) task of MediaEval 2014 contained required participants to a) cluster a collection of images so that the images in each cluster are associated with a distinct social event and b) given a collection of images / clusters corresponding to social events, to retrieve those that match specific criteria. By social events, we mean that the events are planned by people, attended by people and that the media illustrating the events are captured by people. Each image in the dataset is accompanied by metadata typically found on the social web (including time-stamps, tags, geotags for a small subset of them).</div>
<div>&nbsp;</div>
<div>For more information on the SED 2014 dataset, challenges and evaluation, please see the following publication. If you use the dataset for your research, please cite the paper:</div>
<div>&nbsp;</div>
<div>G. Petkos, S. Papadopoulos, V. Mezaris. "Social Event Detection at MediaEval 2014: Challenges, Dataset and Evaluation", Proc. MediaEval 2014 Workshop, Barcelona, Spain, October 2014.</div>
<div>&nbsp;</div>
<div><strong>How to access</strong>:</div>
<div>The dataset has two parts, the first contains a set of 362,578 images that belong to 17,834 events. Its metadata file, in JSON format, can be obtained from here:</div>
<div>&nbsp;</div>
<div>
	<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);"><a href="https://socialsensor.iti.gr/sed2014/SED_2014_Dev_Metadata.rar" search_id="undefined" style="margin: 0px; padding: 0px; border: 0px; font-weight: inherit; font-style: inherit; font-family: inherit; vertical-align: baseline; color: rgb(17, 68, 136);">Metadata file for first part</a></p>
	<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);">&nbsp;</p>
	<div>To obtain the image files please use the URL listed for each image in the metadata file. The association of these images to the events is provided in the following file:&nbsp;</div>
	<div>&nbsp;</div>
	<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);"><a href="http://www.socialsensor.eu/sed2014/SED_2014_Dev_Clusters.rar" search_id="undefined" style="margin: 0px; padding: 0px; border: 0px; font-weight: inherit; font-style: inherit; font-family: inherit; vertical-align: baseline; color: rgb(17, 68, 136);">Cluster mappings file for first part</a></p>
</div>
<div>&nbsp;</div>
<div>This first part of the dataset is used for development in the first subtask as well as for development and testing purposes in the second subtask. In particular, the data in the first part of the dataset can be used as an example clustering for developing solutions to the first subtask. Additionally, for development purposes in the first subtask we provide a list of example queries here:</div>
<div>&nbsp;</div>
<div>
	<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);"><a href="http://www.socialsensor.eu/sed2014/SED_2014_Dev_Queries.rar" search_id="undefined" style="margin: 0px; padding: 0px; border: 0px; font-weight: inherit; font-style: inherit; font-family: inherit; vertical-align: baseline; color: rgb(17, 68, 136);">Development queries file</a></p>
	<div>&nbsp;</div>
	<div>The second part of the dataset is used for testing in the first subtask. The corresponding metadata file can be found here:</div>
</div>
<div>&nbsp;</div>
<div>
	<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);"><a href="http://www.socialsensor.eu/sed2014/SED_2014_Test_Metadata.rar" search_id="undefined" style="margin: 0px; padding: 0px; border: 0px; font-weight: inherit; font-style: inherit; font-family: inherit; vertical-align: baseline; color: rgb(17, 68, 136);">Metadata file for second part</a>&nbsp; (has exactly the same format as the first metadata file)</p>
	<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);">&nbsp;</p>
	<div>The test queries for the second subtask can be found in the following file:</div>
	<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);">&nbsp;</p>
	<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);"><a href="http://www.socialsensor.eu/sed2014/SED_2014_Test_Queries.rar" search_id="undefined" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; color: rgb(17, 68, 136);">Test queries file</a></p>
</div>
<div>&nbsp;</div>
<div>Finally, we provide the ground truth for the first subtask here:</div>
<div>&nbsp;</div>
<div>
	<div>
		<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);"><a href="http://www.socialsensor.eu/sed2014/SED_2014_Subtask1_ground_truth.json" search_id="undefined" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; color: rgb(17, 68, 136);">First subtask ground truth</a></p>
	</div>
	<div>&nbsp;</div>
</div>
<div>And the ground truth for the second subtask here:</div>
<div>&nbsp;</div>
<div>
	<div>
		<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);"><a href="http://www.socialsensor.eu/sed2014/SED_2014_Subtask2_ground_truth.json" search_id="undefined" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; color: rgb(17, 68, 136);">Second subtask ground truth</a></p>
		<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);">&nbsp;</p>
		<h2 style="margin: 0px; padding: 0px; border: 0px; font-size: 17px; font-family: 'Segoe UI', 'Lucida Grande', Arial, sans-serif; vertical-align: baseline; line-height: 1.25em; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);"><span style="font-family: 'Segoe UI', 'Lucida Grande', Arial; font-size: 13px; line-height: 19.5px;">Evaluation:</span></h2>
		<div>A script is provided to easily compute the evaluation measures on your results. You can find it here:</div>
	</div>
	<div>&nbsp;</div>
</div>
<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);"><a href="http://www.socialsensor.eu/sed2014/SED_2014_evaluation_resources.rar" search_id="undefined" style="margin: 0px; padding: 0px; border: 0px; font-weight: inherit; font-style: inherit; font-family: inherit; vertical-align: baseline; color: rgb(17, 68, 136);">Evaluation resources</a></p>
<div>&nbsp;</div>
<div>
	<div>
		<div>The script requires python 2.7. For instructions about how to run this script, please see the details in the ReadMe file that you will find in the above arhive. Please also note that your result files much have the formats below.</div>
		<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);">&nbsp;</p>
		<div>For the first subtask the file must be a plain ASCII file, in which each line represents the association of each image in the test set to a cluster. Each line must have the form "photoID-single tab-eventID". The photoIDs must be the same as those in the test set's metadata file, whereas the eventID can be any string that does not include a tab character. E.g. the following would be part of a valied file:</div>
		<div>&nbsp;</div>
		<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);">3587419916 7081</p>
		<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);">3750102971 7028</p>
		<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);">3740276442 7047</p>
		<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);">9230492703 122</p>
		<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);">1820390101 2080</p>
		<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);">&nbsp;</p>
		<div>For the second subtask the file must be a plain ASCII file, in which each line contains the events retrieved for each of the 10 test queries. Each line must have the form "testQueryID - single tab - comma separated eventIDs". The testQueryIDs must be the same as those in the test queries file, whereas the eventIDs must match those used in the image-event association file. The following is part of a valid submission.</div>
		<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);">&nbsp;</p>
		<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);">Test-1 &nbsp; &nbsp; 279, 2467, 2039, 8945, 2029</p>
		<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);">Test-2 &nbsp; &nbsp;3270, 129, 909, 1010, 5643, 9129, 2198</p>
		<p style="margin: 0px; padding: 0px; border: 0px; font-size: 13px; font-family: 'Segoe UI', 'Lucida Grande', Arial; vertical-align: baseline; line-height: 19.5px; color: rgb(68, 68, 68); background-color: rgb(255, 255, 255);">&nbsp;</p>
		<div>Many thanks to Timo Reuter for providing the largest part of the script, as well as for providing the ReSEED dataset on which a large part of the datasets is based.</div>
		<div>&nbsp;</div>
		<div>
			<div>&nbsp;</div>
			<div><span style="color: rgb(68, 68, 68); font-family: 'Trebuchet MS', Verdana, Arial, sans-serif; line-height: 1.3em; font-size: 8pt; background-color: rgb(255, 255, 255);"><strong>Copyright notice:</strong>&nbsp;The images distributed as part of the Social Event Detection 2014 (SED 2014) dataset were collected from Flickr, where they were posted by their respective owners under a Creative Commons license. The Creative Commons attribution licenses allow for image use as long as the photographer is credited for the original creation. Possibly, use is granted under additional restrictions, but none of these preclude the use of the images for benchmarking purposes.&nbsp;</span><span style="color: rgb(68, 68, 68); font-family: 'Trebuchet MS', Verdana, Arial, sans-serif; font-size: 8pt; line-height: 1.3em; background-color: rgb(255, 255, 255);">While compiling the Social Event Detection 2014 (SED 2014) dataset, we collected only Creative Commons images, and also collected as much information possible about the creators of each image. The creator information, the exact license type and other relevant information are included in the image license file, which is distributed together with the images.&nbsp;</span><span style="color: rgb(68, 68, 68); font-family: 'Trebuchet MS', Verdana, Arial, sans-serif; font-size: 8pt; line-height: 1.3em; background-color: rgb(255, 255, 255);">We would like to take this opportunity to express our gratitude to the image photographers for allowing us to use their pictures: we greatly appreciate this and gladly acknowledge your work. Your names and license details are listed in image license file. Please let us know if you have special wishes on how you would like to be credited or have additional details that must be incorporated.</span></div>
			<div>&nbsp;</div>
		</div>
	</div>
</div>
<p>&nbsp;</p>
