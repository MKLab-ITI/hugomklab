---
excerpt: 'A set of state-of-the-art features associated with the images of the Yahoo Flickr Creative Commons (YFCC) dataset'
types: results
tags:
- data
images: []
layout: results
title: The VLAD-VGG-YFCC Dataset
date: '2015-08-21T12:19:24+03:00'
---
<p>We make available a set of state-of-the-art features associated with the images of the Yahoo Flickr Creative Commons (YFCC) dataset. The features are made available under the <a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0 license</a>.</p>
<p>In particular, we make available the following features:</p>
<ul>
	<li><strong>VGG: </strong>These features were proposed by <a href="http://arxiv.org/abs/1409.1556">Simonyan and Zisserman</a>&nbsp;for the the ILSVRC 2014 challenge and the respective system was ranked second best in the classification task. The features are extracted with a 16-layer CNN and we exploit the output of the last fully connected layer <em>fc7</em>, which consists of 4,096 dimensions. This layer is selected since its neurons convey a relatively high-level encoding of the image content that is well suited for finding semantically similar images for a query. &nbsp;</li>
	<li><strong>VGG-PCA:</strong> Due to the significant cost of the full VGG features in large scale collections, such as YFCC, we also create a PCA compressed version of VGG. The PCA matrix is computed using a sample of 250,000 YFCC images, randomly selected from the collection. We make available representations consisting of the most significant 16 and 128 dimensions from the PCA representation of VGG, denoted respectively as VGG-16 and VGG-128.</li>
	<li><strong>VLAD: </strong>These are <a href="http://lpis.csd.auth.gr/publications/spyromitrosIEEETMM2014.pdf">improved VLAD vectors using SURF</a> and the multiple vocabulary aggregation technique of <a href="https://hal.inria.fr/hal-00722622">Jegou and Chum</a>&nbsp;with four visual vocabularies (of k=128 centroids). Their initial dimensions (32,768) were reduced with PCA+whitening. VLAD-1024, VLAD-128 and VLAD-16 correspond to retaining the 1024, 128 and 16 most significant dimensions respectively.&nbsp;</li>
</ul>
<div>All the features can be downloaded via SFTP using the following details:</div>
<ul>
	<li><em>host:</em> mklab.iti.gr/public/vgg-vlad-yfcc</li>
	<li><em>port:</em> 22</li>
	<li><em>username:</em> vgg</li>
	<li><em>password:</em> 123</li>
</ul>
<div>In case you make use of these features in your work, please cite the following paper:</div>
<p>A. Popescu, E. Spyromitros-Xioufis, S. Papadopoulos, H. Le Borgne, Y. Kompatsiaris. <strong>"Towards an Automatic Evaluation of Retrieval Performance with Large Scale Image Collections"</strong>. In Proceedings of the MMCommons Workshop, co-located with ACM Multimedia, Brisbane, Australia</p>
<p>&nbsp;</p>
