---
excerpt: 'Associating Images with High-Level Semantic Concepts'
types: results
tags:
- demo
images: []
layout: results
title: SVM-based Classification Framework
date: '2007-11-16T16:54:38+02:00'
---
<p>
<b>Associating Images with High-Level Semantic Concepts </b><br />
<br />
The SVM-based classification framework, which came up as a result of ITI's research activity on the knowledge-assisted multimedia analysis research field, supports the automatic image segmentation and semantic annotation at region level. Semantic annotation concerns the association of every image region with pre-defined high-level semantic concepts.
</p>
<p>
<br />
<img src="/files/images/SVM-Classification.jpg" height="544" width="523" />
</p>
<p>
The examined image is initially segmented, using the algorithm proposed in [1], and the following MPEG-7 descriptors are extracted for every resulting region: Scalable Colour, Region Shape, Homogeneous Texture and Edge Histogram.<br />
<br />
The core functionality of the developed framework consists of a Support Vector Machines (SVMs) structure. Specifically, an individual SVM is introduced for every defined high-level concept to detect the corresponding instances based on the calculated low-level descriptors. Each SVM is trained under the ‘one-against-all' approach.<br />
<br />
In the current stage of development, 27 high-level semantic concepts are supported: Natural-Person, Sailing-Boat, Sand, Building, Pavement, Road, Body-Of-Water, Cliff, Cloud, Mountain, Sea, Sky, Stone, Waterfall, Wave, Dried-Plant, Dried-Plant-Snowed, Foliage, Grass, Tree, Trunk, Snow, Sunset, Car, Ground, Lamp-Post, Statue.
</p>
<p>
<a href="/files/SVMClassification.zip">Download</a> an executable version of the developed classification framework.
</p>
<p>
An extension of the provided software, namely an ontology-based unified framework for realizing semantic image analysis and classification, has also been developed and is described in [2].<br />
<br />
[1] V. Mezaris, I. Kompatsiaris and M. G. Strintzis, &quot;Still Image Segmentation Tools for Object-based Multimedia Applications&quot;, International Journal of Pattern Recognition and Artificial Intelligence, vol. 18, no. 4, pp. 701-725, June 2004.<a href="/files/pdf/ijprai04.pdf"><img src="/files/pdf/pdf.png" align="top" border="0" /></a><br />
[2] G. Th. Papadopoulos, V. Mezaris, I. Kompatsiaris and M. G. Strintzis: &quot;Combining Global and Local Information for Knowledge-Assisted Image Analysis and Classification&quot;, EURASIP Journal on Advances in Signal Processing, Special Issue on Knowledge-Assisted Media Analysis for Interactive Multimedia Applications, , vol. 2007 (2007), Article ID 45842.<a href="/files/pdf/jasp07.pdf"><img src="/files/pdf/pdf.png" align="top" border="0" /></a>
</p>
