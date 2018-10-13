---
excerpt: 'A very large collection of forgeries collected from various Web and social media sources, accompanied by ground truth binary masks localizing the forgery, and by the image sources that were used to perform the forgery, wherever these are avaiable.'
types: results
aliases:
- /project/wild-web-tampered-image-dataset
tags:
- data
images: []
layout: results
title: The Wild Web tampered image dataset
date: '2015-11-09T18:03:52+02:00'
---
<p>In our early work on Image Forensics as part of the REVEAL project, we came into an important realization: the real-world forgeries circulating the Web that we were asked to analyze, differed significantly from the images found in the typical evaluation datasets used in most research papers. Most images found on the Web have undergone various post-processing operations, such as resaving and rescaling, which causes most of today's splicing localization algorithms to often perform significantly worse in the real world compared to the performance reported in the bibliography [1].</p>
<div>The Wild Web dataset aims to cover that gap in the evaluation of image tampering localization algorithms. It is a very large collection of forgeries collected from various Web and social media sources, accompanied by ground truth binary masks localizing the forgery, and by the image sources that were used to perform the forgery, wherever these are avaiable. In contrast to other datasets, no unspliced images are contained.</div>
<div>&nbsp;</div>
<div>
	<div><strong>Cases and sub-cases</strong></div>
	<div>The dataset contains 80 cases of forgeries, all confirmed from multiple reliable sources and with the help of the original photographs where available. For many cases, we found that multiple sub-cases exist, where it is not straightforward &nbsp;to identify which was the original forgery and which are later re-modifications. In these cases, we separately kept each possible sub-case. Overall, the dataset contains 90 such sub-cases.</div>
</div>
<div>&nbsp;</div>
<div>
	<div><strong>Collecting images</strong></div>
	<div>For each sub-case, the dataset contains all instances that we could find in the web using the Google and TinEye reverse image search services. We then passed the downloaded files through a hash-based comparison process to filter out exact file duplicates. The entire collection thus currently contains 13,577 unique images.</div>
	<div>&nbsp;</div>
	<div>
		<div><strong>Secondary modifications and croppings</strong></div>
		<div>The dataset is internally separated in one additional level: for each sub-case, we have isolated images where an obvious second splicing or content alteration has taken place (e.g. by adding a watermark), or where a large amount of cropping has occurred. The former case is misleading as most algorithms will detect the second modification -often placed on top of the first, thus accidentally giving a “correctly” localized output. The latter case means that the ground truth mask will not fit properly over the image, and is thus useless. By setting these images aside, the main corpus of the dataset contains 10,870 images.</div>
		<div>&nbsp;</div>
		<div>
			<div><strong>Ground truth masks</strong></div>
			<div>We have manually created ground truth masks for each sub-case. As, in many sub-cases, the forgery concerned multiple areas of the image, we were unsure which one took place first and which area's trace might have remained detectable at the end of the forging process. Thus, for these sub-cases we created multiple different ground-truth masks to reflect this uncertainty. We believe that, for each such sub-case, if an algorithm produces an output that matches any of the masks, this should be considered a successful detection (and should suggest that the corresponding mask is the one that better reflects reality)</div>
			<div>A second consideration when using the ground-truth masks is the fact that the images we have downloaded do not all have the same dimensions for each sub-case. Many resized versions exist, and it is nearly impossible to identify which one is the oldest. However, since we have removed the cropped versions, the binary mask can in each case be resized to match the image size -even in cases where the image has been rescaled nonuniformly, this resizing operation will still produce a valid ground-truth mask for the image.</div>
			<div>&nbsp;</div>
			<div>
				<div><strong>Dataset organization</strong></div>
				<div>The dataset root contains two folders: WildWeb and &nbsp;UnsplicedSources. The former contains 90 subfolders, each containing one subcase. The naming convention is, in all cases, the name of the case, followed by a number if multiple subcases exists. Thus, KerryLaVey is the only subcase of KerryLaVey, while ObamaSmoking1 is the first subcase of ObamaSmoking. Within each such folder are the images, plus two subdirectories. The first subdirectory, called Mask contains all the mask files for the subcase, in the form of PNG images, with white (255) corresponding to the tampered region and black (0) to the rest of the image pixels. The second subdirectory, called Crops – PostSplices, contains all cropped and re-spliced versions of the subcase.</div>
				<div>Finally, the UnsplicedSources folder contains 71 subfolders, each named after a case, containing the source images from which the splice was performed and some text explaining the history of the forgery and the articles confirming the forgery. The reason there are fewer sources (71) than cases (80) is that we have certain cases originating from the same sources, but conducted at different times, and with different localizations, which we have registered as entirely separate cases.</div>
				<div>&nbsp;</div>
				<div>
					<div><strong>Acquiring the Wild Web dataset</strong></div>
					<div>Due to copyright considerations, we cannot make the Wild Web dataset publicly available. However, if you would like to use it for research purposes, we will be happy to share the entire dataset. Email markzampoglou@iti.gr and papadop@iti.gr and we will provide you with a download link (~910MB).</div>
					<div>&nbsp;</div>
					<div><strong>Citing the dataset</strong></div>
					<div>If you use the dataset, please cite the following publication:</div>
					<div>[1] M. Zampoglou, S. Papadopoulos, and Y. Kompatsiaris. "<a href="http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=7169839">Detecting image splicing in the wild (Web).</a>" In Multimedia &amp; Expo Workshops (ICMEW), 2015 IEEE International Conference on, pp. 1-6. IEEE, 2015.</div>
					<div>&nbsp;</div>
				</div>
			</div>
			<div>&nbsp;</div>
		</div>
		<div>&nbsp;</div>
	</div>
</div>
<div>&nbsp;</div>
<div>&nbsp;</div>
