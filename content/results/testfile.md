---
excerpt: 'TEst file'
types: results
tags:
- material
images: []
layout: results
title: TEST material
date: '2015-10-09T12:36:44+03:00'
---
<p><font size="5" color="red"><strong>Accelerated Kernel Subclass Discriminant Analysis and SVM combination:</strong></font><em><font size="4" color="red"> An efficient dimensionality reduction and classification method, for very high-dimensional data.</font></em></p>
<p><strong>Description </strong></p>
<p>AKSDA is a new, GPU-accelerated, state-of-the-art C++ method (provided both as source code and command-line executable) for supervised dimensionality reduction and classification, using multiple kernels. It greatly reduces the dimensionality of the input data, while at the same time it increases their linear separability. Used in conjunction with linear SVMs, it achieves state-of-the-art classification results, consistently higher than Kernel SVM approaches, at orders-of-magnitude shorter training times.</p>
<p>Use AKSDA to make full use of your (even low-end!) Nvidia GPU, to accelerate your classification or quickly reduce the dimensionality of any data, and achieve higher accuracy and reduced training times (in most cases shorter than those of current state-of-the-art linear SVMs)!</p>
<p>AKSDA takes as input an annotated training set (both for binary and multiclass problems) and a test set. It will reduce the dimensionality of the feature vectors provided for the training and testing sets using any number of the available kernels. The resulting projected data can be used to train (on the training set) and apply (on the test set) a linear SVM classifier, which will result in an increase in classification performance, at a fraction of the time required by other state-of-art SVM methods. Its output is both the final linear SVM classification result and the projection of the original input data in the reduced dimension.</p>
<p>In essence, this complete method can:</p>
<div style="margin-left:20.5pt;background:#FFFFFF; border: 3px solid navy;text-align:center">
	<ul>
		<li>Accelerate classification by directly replacing any SVM classifier (which would typically be trained and applied on the original, high-dimensional feature vectors), or by using AKSDA just as a preprocessing (dimensionality reduction) step that you can then pair with any kind of classifier.</li>
		<li>Perform fast and effective dimensionality reduction, by replacing any other supervised dimensionality reduction technique in other applications, such as data visualization, k-means clustering, Nearest Neighbor search etc.</li>
	</ul>
</div>
<br>
<p><strong>Usage</strong></p>
<ol>
	<li>Download the <a href="#Downloads"><strong>aksda.rar </strong></a>from the list below.</li>
	<li>Unpack the <a href="#Downloads"><strong>aksda.rar </strong></a>archive creating a new folder.</li>
	<li>Run the software&nbsp;or use the .dll/.lib to link AKSDA as a plug-in library on a project of your own, following the instructions in the included “AKSDA documentation.docx" file.</li>
</ol>
<p><strong>Output</strong></p>
<ol>
	<li>Classification: This program outputs in a .txt the predictions for the test samples, as would any classic SVM classifier. &nbsp;The predictions have columns equal to the number of classes if classes&gt;2. For binary classification, the output is only 1 column. Each &nbsp;row corresponds to one sample, and each column holds the probability value (or simple decision value), that the sample will belong to a specific class.</li>
	<li>Dimensionality reduction: This method will also output the input data projected in a much lower dimension, typically to the size of (<strong>N*M</strong>-2) elements per sample, where <strong>Ν</strong> is the number of classes and <strong>M </strong>is any number of requested subclasses per class. It has been successfully used to reduce 100K-element vectors to a dimension of 2, while still increasing the classification accuracy beyond state-of-art performance.</li>
</ol>
<p><strong>Main prerequisites </strong></p>
<ul>
	<li>CPU with at least 4 cores.</li>
	<li>Windows (7 or later) x64.</li>
	<li>CUDA-capable GPU with compute capability 3.0 or more. [<a href="https://developer.nvidia.com/cuda-gpus">What is the compute capability of MY GPU?</a>]</li>
</ul>
<p><strong>Version history</strong></p>
<p>Release version (v 2.4, released 2016-6-9):&nbsp;&nbsp; Updated dead links in documentation. Cleaner source code, more comments.</p>
<p>Release version (v 2.3, released 2016-4-12): Bugfixes on numerical stability, visual output. Removal of some obsolete messages.</p>
<p>Release version (v 2.2, released 2016-3-10): Bugfixes (mostly visual/output), more helper functions available.</p>
<p>Release version (v 2.1, released 2016-2-25): Various minor Bug fixes.</p>
<p>Release version (v 2.0, released 2016-2-12): Multiclass, multikernel capabilities. Unrestricted, full version.</p>
<p>Demo version (v1.0.1, released 2015-11-25): Improved speed and memory consumption. Supports 4 total precision options. Incorporates the changes of Eigen 3.2.7</p>
<p>Demo version (v1.0.0, released 2015-10-09)</p>
<p><a name="Downloads"><strong>Downloads</strong></a></p>
<p>Latest Edition (v 2.4)</p>
<ul>
	<li><a href="http://mklab.iti.gr/files/AKSDAv2.4.rar">AKSDA.rar</a> <strong>: 64-bit Windows (7 or later)</strong></li>
</ul>
<p><strong>Publications </strong></p>
<p>This software is the AGSDA implementation presented in the following paper:</p>
<p><span lang="EN-US">S. Arestis-Chartampilas, N. Gkalelis, V. Mezaris, "AKSDA-MSVM: a GPU-accelerated multiclass learning framework for multimedia", Proc. ACM Multimedia 2016, Amsterdam, The Netherlands, Oct. 2016.</span></p>
<p>It is an extension of the earlier method presented in:</p>
<p><span lang="EN-US">S. Arestis-Chartampilas, N. Gkalelis, V. Mezaris, "GPU accelerated generalised subclass discriminant analysis for event and concept detection in video", Proc. ACM Multimedia 2015, Brisbane, Australia, Oct. 2015 </span>[<a href="http://www.iti.gr/~bmezaris/publications/mm15_preprint.pdf">download link</a>]</p>
<p>If you find this software useful in your research work, please cite the above paper(s).</p>
<p><strong>License </strong></p>
<p>Every individual piece of software or source code used to make this trial version has its own license that applies. Look below for more info.</p>
<p style="margin-left:21.3pt;">Cuda has its own license (<a href="http://docs.nvidia.com/cuda/eula/index.html#nvidia-cuda-toolkit-license-agreement">http://docs.nvidia.com/cuda/eula/index.html#nvidia-cuda-toolkit-license-agreement</a>) which you might have already agreed to, by installing their toolkit and drivers in the “dependencies” folder.</p>
<p style="margin-left:21.3pt;">Eigen is MPL2 with some features under different licensing (<a href="http://eigen.tuxfamily.org/index.php?title=Main_Page#License">http://eigen.tuxfamily.org/index.php?title=Main_Page#License</a>). Eigen’s license dictates that we clearly provide a way to access their source code. Their source code can be obtained freely in <a href="http://eigen.tuxfamily.org/index.php?title=Main_Page">http://eigen.tuxfamily.org/index.php?title=Main_Page</a> .</p>
<p style="margin-left:21.3pt;">Libsvm (<a href="http://www.csie.ntu.edu.tw/~cjlin/libsvm/COPYRIGHT">http://www.csie.ntu.edu.tw/~cjlin/libsvm/COPYRIGHT</a>)</p>
<p style="margin-left:21.3pt;">Liblinear (<a href="http://www.csie.ntu.edu.tw/~cjlin/liblinear/COPYRIGHT">http://www.csie.ntu.edu.tw/~cjlin/liblinear/COPYRIGHT</a>)</p>
<p style="margin-left:21.3pt;">Opencv (3-clause BSD License) (<a href="http://opencv.org/license.html">http://opencv.org/license.html</a>)</p>
<p style="margin-left:21.3pt;">Vlfeat (BSD license) (<a href="http://www.vlfeat.org/license.html">http://www.vlfeat.org/license.html</a>)</p>
<p style="margin-left:21.3pt;"><strong>Downloading, copying, installing or using any part of our software</strong> implies you have read, understood, and agreed upon, every license presented in this document (each applying to its own product). If the links are inaccessible, we provide a separate folder named “licenses” in <strong>aksda.rar</strong> containing copies of every one of them.</p>
<hr>
<p><strong>Our software </strong>(AKSDA) is covered by the <a>following license</a>: Copyright (C) 2015 Stavros Arestis-Chartampilas, Nikolaos Gkalelis, Vasileios Mezaris / CERTH-ITI. All Rights Reserved.</p>
<p>The AKSDA software, including the provided executables, source code, documentation and all other materials (excluding third-party software, for which separate licenses apply, as specified above and in the respective web pages), is provided only for academic, non-commercial use. Commercial use is prohibited. For information on non-academic use possibilities, please contact <a href="mailto:bmezaris@iti.gr">bmezaris@iti.gr</a>.&nbsp;</p>
<p>This software is provided by the authors "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. In no event shall the authors be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage. No warranty or representation of any kind is made, given or implied as to the absence of any infringement of any proprietary rights of third parties.</p>
<hr>
<p>&nbsp;</p>
<p><strong>Acknowledgements</strong></p>
<p>This work was supported by the EC under contracts FP7-600826 ForgetIT and H2020-687786 InVID, and by Nvidia Corporation with the donation of a Tesla K40 GPU.</p>
<p><strong>Contacts </strong></p>
<p>You may contact Vasileios Mezaris by sending e-mail at <a href="mailto:bmezaris@iti.gr">bmezaris@iti.gr</a> for any question or remark you may have with respect to this tool.</p>
