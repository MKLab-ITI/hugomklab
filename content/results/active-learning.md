---
excerpt: 'Active learning is a machine learning variant that opts to overcome the problem of gathering a training corpus due to the need for manual annotation'
types: results
tags:
- tool
images: []
layout: results
title: Active Learning
date: '2016-08-31T15:51:45+03:00'
---
<p>This toolbox facilitates the application of active learning in multimedia data. &nbsp;Active learning is a machine learning variant that opts to overcome the problem of gathering a training corpus due to the need for manual annotation. In an effort to minimize the labeling effort, active learning proposes to train an initial classifier with a very small set of labeled examples and then expand the training set by selectively sampling new examples from a much larger set of unlabeled examples (also known as pool of candidates). These examples are selected based on their informativeness, i.e. how much they are expected to improve the classifier's performance. They are found in the uncertainty areas of the classifier and, in a typical case, are annotated upon request by an errorless oracle.</p>
<p>In the case of image classification, flickr offers an abundant set of user tagged images, which if used in the pool of candidates can automate the process of active learning. In this direction, we propose a method, SALIC (for details see the <a href="http://mklab.iti.gr/research/multimedia">here</a>), that uses tagged images as the pool of candidates and selects the images that are both of maximum informativess as well as accurately predicted for their content based on their tags. This toolbox also implements SALIC, in addition to the typical active learning method and a tag-based oracle.</p>
<p>&nbsp;</p>
<p><strong>Usage:</strong></p>
<ul>
	<li>Clone the project from GitHub [<a href="https://github.com/MKLab-ITI/salic">link</a>].</li>
	<li>Install the requirements (details are included in the README file, also copied below)</li>
	<li>Download the datasets&nbsp;and modify Wrapper.m based on the comments in it (paths to datasets, etc.) and run Wrapper.m (This will execute SALIC by default)</li>
</ul>
<p><strong>Output:</strong></p>
<ul>
	<li>The toolbox will compute visual and textual features. The path and files where the features will be saved are defined in the Wrapper.m file.</li>
	<li>The average precision variable (AP) will be returned by Wrapper.m. It is a matrix of size #concepts x # iterations including the average precision of the classifiers for each concept and iteration</li>
	<li>A plot with the mAP values over each iteration</li>
</ul>
<p>&nbsp;</p>
<div><strong>Installation:</strong></div>
<ol>
	<li>Clone the repository</li>
	<li>Download and compile LIBSVM for your architecture https://www.csie.ntu.edu.tw/~cjlin/libsvm/</li>
	<li>Download and compile the ConvNet Feature Computation Package from http://www.robots.ox.ac.uk/~vgg/software/deep_eval/</li>
	<li>Change the paths to the folders including the datasets in Wrapper.m, create the required files (img_Files.mat, tag_files.mat for each dataset) and run Wrapper.</li>
</ol>
<div>&nbsp;</div>
<div><strong>Requirements:</strong></div>
<ol>
	<li>There is only compatability for Linux (the ConvNet Feature Computation Package is not compatible with windows). If a different CNN feature extraction library is used that runs on Windows, the code should run on Windows as well (not tested)</li>
	<li>For MIRFLICKR (1m images as the pool dataset), 64GB of RAM is minimum</li>
	<li>The code was tested using Matlab 2012a</li>
</ol>
<div>&nbsp;</div>
<div><strong>Publication</strong></div>
<div>&nbsp;</div>
<div>If you use this code cite the following paper:</div>
<div>&nbsp;</div>
<div>E. Chatzilari, S. Nikolopoulos, Y. Kompatsiaris and J. Kittler, "SALIC: Social Active Learning for Image Classification," in&nbsp;<em>IEEE Transactions on Multimedia</em>, vol. 18, no. 8, pp. 1488-1503, Aug. 2016.<br>
	doi: 10.1109/TMM.2016.2565440</div>
<div>&nbsp;</div>
<div>URL: https://doi.org/10.1109/TMM.2016.2565440</div>
<div>&nbsp;</div>
<p><strong>License</strong></p>
<div>Copyright 2016 Elisavet Chatzilari</div>
<div>&nbsp;</div>
<div>&nbsp; &nbsp;Licensed under the Apache License, Version 2.0 (the "License");</div>
<div>&nbsp; &nbsp;you may not use this file except in compliance with the License.</div>
<div>&nbsp; &nbsp;You may obtain a copy of the License at</div>
<div>&nbsp;</div>
<div>&nbsp; &nbsp; &nbsp; &nbsp;http://www.apache.org/licenses/LICENSE-2.0</div>
<div>&nbsp;</div>
<div>&nbsp; &nbsp;Unless required by applicable law or agreed to in writing, software</div>
<div>&nbsp; &nbsp;distributed under the License is distributed on an "AS IS" BASIS,</div>
<div>&nbsp; &nbsp;WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.</div>
<div>&nbsp; &nbsp;See the License for the specific language governing permissions and</div>
<div>&nbsp; &nbsp;limitations under the License.</div>
<div>&nbsp;</div>
<div>&nbsp;</div>
<div><strong>Acknowledgements</strong></div>
<div>&nbsp;</div>
<div>This work was supported by the European Community's Seventh Framework Programme (FP7) under Grant FP7-ICT-600676 “i-Treasures: Intangible Treasures—Capturing the Intangible Cultural Heritage and Learning the Rare Know-How of Living Human Treasures” and Grant FP7-601138 “PERICLES Digital Preservation.”</div>
<div>&nbsp;</div>
<div><strong>Contacts</strong></div>
<div>&nbsp;</div>
<div>You may contact Elisavet Chatzilari by sending e-mail at ehatzi@iti.gr for any question or remark you may have with respect to this tool.</div>
