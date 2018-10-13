---
excerpt: 'Aim of this framework is the investigation of the behavior and the resulting performance of different spatial context exploitation techniques for different combinations of classifiers and low-level features'
types: results
tags:
- data
- image set
images: []
layout: results
title: Spatial Context Evaluation Framework
date: '2009-02-13T13:47:16+02:00'
---
<p>
<strong>Framework description</strong>
</p>
<p>
Aim of this framework is the
investigation of the behavior and the resulting performance of different
spatial context exploitation techniques for different combinations of classifiers
and low-level features. The framework has been developed in collaboration with the <a href="http://isweb.uni-koblenz.de/"><strong>ISWeb - Information Systems and Semantic Web</strong></a> Research Group at the Institute for
Computer Science, University
of Koblenz-Landau, within
the EU-funded <a href="http://www.k-space.eu/"><strong>K-Space</strong></a> research project.
</p>
<p>
<!--break-->In this work, two approaches making use
of spatial knowledge for semantic image analysis are comparatively evaluated.
The first one is based on a Genetic Algorithm (GA), which is employed in order to decide upon the optimal semantic image interpretation by treating semantic image analysis as a global optimization problem. On the other hand, the second method follows a Binary Integer Programming (BIP) technique for estimating the optimal solution. Initially, the examined image is segmented and two individual sets of low-level
descriptors are extracted for every resulting segment. In parallel to this
procedure, for every pair of image regions a corresponding set of fuzzy
directional spatial relations are estimated. Then, the computed descriptors are
provided as input to two different classifiers, namely a Support Vector Machine
(SVM)- and a Maximum Likelihood (ML)-based one, in order to associate every
region with a predefined high-level semantic concept based solely on visual
information. The latter is used for denoting a real-world object that can be
present in the examined image. Consequently, the two aforementioned spatial
context techniques, which perform on top of the initial classification results
and which make use of the available spatial knowledge, are applied in order to
estimate an optimal region-concept assignment. The reported experimental
results demonstrate the improvements attained using spatial context in a number
of different image analysis schemes.
</p>
<p>
&nbsp;
</p>
<p>
<strong>Data</strong>
</p>
<p>
The image set utilized
in this work was provided by Alinari 24 ORE
(<a href="http://www.alinari.com/">http://www.alinari.com</a>, info: <a href="mailto:euproject-2@alinari.it">euproject-2@alinari.it</a>). The dataset includes: a) the utilized image set, b) the
image segmentation masks, c) region-level manual image annotation, d) the
extracted low-level features, e) the computed fuzzy directional spatial
relations, and f) the region classification results based solely on visual information.
</p>
<p>
<a href="/files/spatialContextEvaluationFramework.zip">Download</a> the
developed framework. 
</p>
<p>
Note: The dataset is publicly available for non-commercial use.
Please refer to 
<a href="/files/pdf/wiamis09-papadopoulos.pdf">
[Papadopoulos et al., <em> Proc. WIAMIS'09, London, UK</em>]</a>
if this dataset is used for experimentation in publications. 
</p>
<p>
&nbsp;
</p>
<p align="center">
<strong>Indicative region-concept
association results</strong>
</p>
<table border="1" cellspacing="0" cellpadding="0">
	<tbody>
		<tr>
			<td width="40" valign="top">
			<p>
			&nbsp;
			</p>
			</td>
			<td width="250">
			<p align="center">
			Input
			image
			</p>
			</td>
			<td width="250">
			<p align="center">
			Region
			classification
			</p>
			</td>
			<td width="250">
			<p align="center">
			Spatial
			context
			</p>
			</td>
		</tr>
		<tr>
			<td width="40">
			<p>
			a)
			</p>
			</td>
			<td width="220">
			<p align="center">
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/00488.jpg" border="0" alt="" width="249" height="381" />
			</p>
			</td>
			<td width="220">
			<p align="center">
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/00488-classification.jpg" border="0" alt="" width="249" height="381" />
			</p>
			</td>
			<td width="220">
			<p align="center">
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/00488-context.jpg" border="0" alt="" width="249" height="381" />
			</p>
			</td>
		</tr>
		<tr>
			<td width="40">
			<p>
			b)
			</p>
			</td>
			<td width="220" valign="top">
			<p>
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/01099.jpg" border="0" alt="" width="249" height="188" />
			</p>
			</td>
			<td width="220" valign="top">
			<p>
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/01099-classification.jpg" border="0" alt="" width="249" height="188" />
			</p>
			</td>
			<td width="220" valign="top">
			<p>
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/01099-context.jpg" border="0" alt="" width="249" height="188" />
			</p>
			</td>
		</tr>
		<tr>
			<td width="40">
			<p>
			c)
			</p>
			</td>
			<td width="220" valign="top">
			<p>
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/00207.jpg" border="0" alt="" width="249" height="188" />
			</p>
			</td>
			<td width="220" valign="top">
			<p>
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/00207-classification.jpg" border="0" alt="" width="249" height="188" />
			</p>
			</td>
			<td width="220" valign="top">
			<p>
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/00207-context.jpg" border="0" alt="" width="249" height="188" />
			</p>
			</td>
		</tr>
		<tr>
			<td width="40">
			<p>
			d)
			</p>
			</td>
			<td width="220" valign="top">
			<p>
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/00439.jpg" border="0" alt="" width="249" height="188" />
			</p>
			</td>
			<td width="220" valign="top">
			<p>
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/00439-classification.jpg" border="0" alt="" width="249" height="188" />
			</p>
			</td>
			<td width="220" valign="top">
			<p>
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/00439-context.jpg" border="0" alt="" width="249" height="188" />
			</p>
			</td>
		</tr>
		<tr>
			<td width="40">
			<p>
			e)
			</p>
			</td>
			<td width="220" valign="top">
			<p>
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/00141.jpg" border="0" alt="" width="249" height="188" />
			</p>
			</td>
			<td width="220" valign="top">
			<p>
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/00141-classification.jpg" border="0" alt="" width="249" height="188" />
			</p>
			</td>
			<td width="220" valign="top">
			<p>
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/00141-context.jpg" border="0" alt="" width="249" height="188" />
			</p>
			</td>
		</tr>
		<tr>
			<td width="40">
			<p>
			f)
			</p>
			</td>
			<td width="220" valign="top">
			<p>
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/00555.jpg" border="0" alt="" width="249" height="330" />
			</p>
			</td>
			<td width="220" valign="top">
			<p>
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/00555-classification.jpg" border="0" alt="" width="249" height="330" />
			</p>
			</td>
			<td width="220" valign="top">
			<p>
			<!--[if gte vml 1]>
			<![endif]--><img src="/files/00555-context.jpg" border="0" alt="" width="249" height="330" />
			</p>
			</td>
		</tr>
	</tbody>
</table>
<p>
Indicative region-concept association
results for the following feature-classifier-spatial context exploitation
technique combinations: a) MPEG-7-ML-BIP, b) MPEG-7-ML-GA, c) MPEG-7-SVM-BIP,
d) MPEG-7-SVM-GA, e) wavelet-ML-BIP, and f) wavelet-ML-GA.
</p>
<p align="center">
<strong> </strong>
</p>
<p align="center">
<strong>Concept detection accuracy</strong>
</p>
<p align="center">
<!--[if gte vml 1]>
<![endif]--><img src="/files/MPEG-SVM-results2.jpg" border="0" alt="" width="500" height="267" /> 
</p>
<p align="center">
<!--[if gte vml 1]>
<![endif]--><img src="/files/MPEG-ML-results2.jpg" border="0" alt="" width="500" height="267" />
</p>
<p align="center">
<img src="/files/WAVELET-ML-results2.jpg" border="0" alt="" width="500" height="267" />
</p>
<p>
Concept detection accuracy (c1: Building,
c2: Foliage, c3: Mountain, c4: Person, c5: Road, c6: Sailing-boat, c7: Sand,
c8: Sea, c9: Sky and c10: Snow).
</p>
<p>
&nbsp;
</p>
<p>
<strong>Publications</strong>
</p>
<p>
G. Th.
Papadopoulos, C. Saathoff, M. Grzegorzek, V. Mezaris, I. Kompatsiaris, S. Staab
and M. G. Strintzis, &quot;Comparative Evaluation of Spatial Context Techniques
for Semantic Image Analysis&quot;, <em>10th International Workshop on Image
Analysis for Multimedia Interactive Services (WIAMIS 2009)</em>, London, UK,
accepted for publication. <a href="/files/pdf/wiamis09-papadopoulos.pdf"><img src="/files/pdf/pdf.png" border="0" alt="" align="top" /></a>
</p>
