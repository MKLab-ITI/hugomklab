---
excerpt: 'Image Aesthetic Quality assessment tool: A Matlab implementation of the feature extraction process of the Image Aesthetic Quality assessment method'
types: results
tags:
- tool
images: []
layout: results
title: IAQ
date: '2015-05-18T15:29:14+03:00'
---
<p><strong>Image Aesthetic Quality</strong> assessment<strong> </strong>tool – This is a Matlab implementation of the feature extraction process of the Image Aesthetic Quality assessment method presented below. This method represents each image according to a set of photographic rules and extracts five representative feature vectors which describe the photo’s simplicity, colorfulness, sharpness, pattern and composition, in order to assess the total aesthetic quality of the image.&nbsp;</p>
<p><strong>Abstract:</strong> &nbsp;This is a comprehensive Image Aesthetic Quality assessment method that represents each image-photo according to a set of photographic rules. Specifically, our method exploits information derived from both low- and high-level analysis of photo layout, not only for the photo as a whole but also for specific spatial regions of it. Five feature vectors are introduced for describing the photo’s simplicity, colorfulness, sharpness, pattern and composition. Subsequently, they are concatenated in a final feature vector where a Support Vector Machine classifier is applied in order to perform the aesthetic quality evaluation. The experimental results and comparisons show that our approach achieves consistently more accurate quality assessment than the relevant literature methods and also that the proposed features can be combined with other generic image features so as to enhance the performance of previous methods.</p>
<p>For more detailed information, please refer to the following paper:</p>
<p>E. Mavridaki, V. Mezaris, "A comprehensive aesthetic quality assessment method for natural image using basic rules of photography”, Proc. IEEE International Conference on Image Processing (ICIP 2015), Quebec, Canada, September 2015.</p>
<p><strong>Description: &nbsp;</strong>A Matlab implementation of the feature extraction process of the aforementioned Image Aesthetic Quality assessment method is attached below (Image_Aesthetic_Quality_CERTH.zip). The input of this software is the path of the folder that contains the images and the output is five text files with the corresponding feature vectors of each examined rule of photography. These feature vectors can be used individually to capture the simplicity, the colorfulness, the sharpness, the existence of pattern and the layout composition of the photo.&nbsp;</p>
<p>The SVM models which were trained using these features for each of the three datasets presented at ICIP 2015 are available for comparison purposes upon request.&nbsp;</p>
<p><strong>Instructions: </strong></p>
<p>Run the ImageAestheticQuality.m which has the following requirements</p>
<p>Input:</p>
<ol>
	<li>imagepath &nbsp;: &nbsp; &nbsp; &nbsp; &nbsp;The path of the folder where the photos are stored. &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</li>
	<li>label &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;: &nbsp; &nbsp; &nbsp; &nbsp;A&nbsp;label for&nbsp;the&nbsp;feature vectors (1 or -1)&nbsp;. Feature vectors are in format&nbsp;compatible with LIBSVM.&nbsp;The LIBSVM format of training and testing data file is: "&lt;label&gt; &lt;index1&gt;:&lt;value1&gt; &lt;index2&gt;:&lt;value2 &gt; ...&nbsp;&lt;indexN&gt;:&lt;valueN&nbsp;&gt;". &nbsp;For classification, &lt;label&gt; is an integer (1 or -1) indicating the class label. The pair &lt;index&gt;:&lt;value&gt; is a feature, &lt;index&gt; is an integer starting from 1 and &lt;value&gt; is a real number indicating the feature value. For testing, &lt;label&gt; is only used to calculate accuracy or errors. If they are unknown, just fill the first column with any numbers.</li>
</ol>
<p>Output:</p>
<ol>
	<li>Simplicity.txt &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;:&nbsp; Simplicity feature vector</li>
	<li>Colorfulness.txt&nbsp;&nbsp;&nbsp;&nbsp;:&nbsp; Colorfulness feature vector</li>
	<li>Sharpness.txt&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:&nbsp; Sharpness feature vector</li>
	<li>Pattern.txt &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;:&nbsp; Pattern feature vector</li>
	<li>Composition.txt &nbsp; &nbsp;:&nbsp; Composition feature vector</li>
</ol>
<p>The aforementioned feature vectors will be stored in the "Results" output folder.&nbsp;The present implementation has been tested on Matlab 2013a.</p>
<p><strong>Publication: </strong></p>
<p>If you use the CERTH image aesthetic quality assessment method in your research work, please cite the following paper:</p>
<p>E. Mavridaki, V. Mezaris, "A comprehensive aesthetic quality assessment method for natural image using basic rules of photography”, Proc. IEEE International Conference on Image Processing (ICIP 2015), Quebec, Canada, September 2015.</p>
<p><strong>License:</strong></p>
<p>Copyright (c) 2015, Mavridaki Eftichia, Mezaris Vasileios and other copyright holders.</p>
<p>All rights reserved.</p>
<p>THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NON-INFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.</p>
<p>Further details of this license can be found in LICENSE.pdf.</p>

### Attachments:
[LICENSE.pdf](/files/LICENSE.pdf)

[Image Aesthetic Quality CERTH - (UPDATED 27/06/2016)](/files/Image_Aesthetic_Quality_CERTH_0.zip)
