---
excerpt: 'A visual search index for the Yahoo! corpus of 100M CC-licensed images (and videos)'
types: results
tags:
- data
images: []
layout: results
title: Visual features and search index for Flickr 100M corpus
date: '2015-01-19T14:41:24+02:00'
---
<p>We are happy to announce the availability of a valuable resource for the Multimedia and Computer Vision community: a visual search index for the <a href="http://yahoolabs.tumblr.com/post/89783581601/one-hundred-million-creative-commons-flickr-images">Yahoo! corpus of 100M CC-licensed images</a> (and videos). The search index is based on state-of-the-art visual features (SURF+VLAD) and indexing techniques (Product Quantization) and is accompanied by an <a href="https://github.com/socialsensor/multimedia-indexing">open-source Java project</a> that can be used to perform rapid visual similarity search operations on the index. The feature extraction was possible in short time with the help of Amazon Web Services (AWS), in particular the Elastic Map-Reduce (EMR) service. Simple wrapper code is included in the aforementioned project and could be used by anyone to perform feature extraction over massive image collections using EMR.</p>
<p>Having the possibility to search fast (in less than one second, see <a href="http://mklab.iti.gr/files/yfcc100M-report.pdf">short report</a>) through such a large index of images could be potentially useful for a number of multimedia analysis tasks, in which nearest neighbour search is one of the key components: image annotation, landmark detection, geolocation estimation, etc.&nbsp;</p>
<div><strong>Download instructions</strong></div>
<div>To make use of the index you need to download the index itself from this <a href="http://mklab.iti.gr/datasets/yfcc100m/yfcc100m_ivfpq.zip">link</a> (~24GB) and a number of "learning" files (see instructions below) from this <a href="http://mklab.iti.gr/datasets/yfcc100m/learning_files.zip">link</a>.</div>
<div>&nbsp;</div>
<div><strong>How to use</strong></div>
<div>The <a href="https://github.com/MKLab-ITI/multimedia-indexing/blob/master/src/main/java/gr/iti/mklab/visual/examples/YFCC100MExample.java">YFCC100MExample</a> Java class of the <a href="https://github.com/MKLab-ITI/multimedia-indexing">multimedia-indexing project</a> gives an example of how a precomputed IVFPQ index of the YFCC100M collection can be loaded and used to answer queries using the multimedia-indexing library that was developed within the <a href="http://socialsensor.eu/">SocialSensor</a> EU Project.</div>
<div>&nbsp;</div>
<div>The main method of the class takes six command line arguments:</div>
<div>- path to the folder where the IVFPQ index resides,</div>
<div>- number of images (i.e. vectors) to load. This number should be equal or smaller to the total size of the index (95,213,780),</div>
<div>- path to the folder where the learning files reside,</div>
<div>- path to a file that contains the URLs of the query images, one URL per row,</div>
<div>
	<div>- number of coarse quantizer lists to be searched out of 8192. Use small values to decrease query time (e.g. 1 or 2 when the full index is loaded to obtain query times less than 1 sec),</div>
	<div>- the size of the cache in Megabytes. Larger values decrease name look-up time but increase memory requirements (typival values are 1024 or 2048),</div>
</div>
<div>and performs the following operations:</div>
<div>- the IVFPQ index is loaded in memory (could take up to 2 hours if you load the whole collection depending on your hardware configuration),</div>
<div>- the coarse and product quantizer are loaded from the learning folder,</div>
<div>
	<div>- an image vectorizer is initialized (i.e. codebooks and PCA matrix are loaded).</div>
	<div>- a text file with one image URL per line is parsed and for each URL:</div>
	<div>-- the image is downloaded,</div>
	<div>-- the image is vectorized and the vector is used to query the index,</div>
	<div>-- 30 most similar images are downloaded and printed along with their distances from the query.&nbsp;</div>
	<div>&nbsp;</div>
	<div>Depending on the number of images that are loaded, a sufficient amount of memory should be allocated using the -Xmx command (use -Xmx16g to load the full collection).</div>
</div>
<div>&nbsp;</div>
<div><strong>How to cite</strong></div>
<div>If you use this dataset in your research, please cite the following paper:</div>
<div>E. Spyromitros-Xioufis, S. Papadopoulos, Y. Kompatsiaris, G. Tsoumakas, I. Vlahavas, "<a href="http://ieeexplore.ieee.org/xpl/freeabs_all.jsp?arnumber=6847226&amp;tag=1&amp;abstractAccess=no&amp;userType=inst">A Comprehensive Study over VLAD and Product Quantization in Large-scale Image Retrieval</a>", IEEE Transactions on Multimedia 16(6), pp. 1713-1728, October 2014.</div>
<div>&nbsp;</div>
<div><strong>Contact</strong></div>
<div>If you have any questions or needs, please get in touch with Symeon Papadopoulos (papadop) or Eleftherios Spyromitros-Xioufis (espyromi), both at @iti.gr. For questions related to the deployment of feature extraction on AWS EMR, get in touch with Katerina Andreadou (kandreadou).</div>
<p>This research has been supported by the <a href="http://socialsensor.eu/">SocialSensor</a> and <a href="http://revealproject.eu/">REVEAL</a> projects.&nbsp;</p>
