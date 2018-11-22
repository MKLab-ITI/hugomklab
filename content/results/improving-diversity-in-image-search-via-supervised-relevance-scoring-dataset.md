---
excerpt: ' MediaEval 2014 Retrieving Diverse Social Images dataset that we used in our experiments'
types: results
tags:
- data
images: []
layout: results
title: Improving Diversity in Image Search via Supervised Relevance Scoring (Dataset)
date: '2017-01-20T16:41:26+02:00'
---
<p>&nbsp;</p>
<p style="text-align: center;"><img alt="" src="http://mklab.iti.gr/datasets/diversity/diversity.jpg" style="width: 480px; height: 151px;"></p>
<p><strong>Abstract&nbsp;</strong></p>
<p>Results returned by commercial image search engines should include relevant and diversified depictions of queries in order to ensure good coverage of users' information needs. While relevance has drastically improved in recent years, diversity is still an open problem. In this paper we propose a reranking method that could be implemented on top of such engines in order to provide a better balance between relevance and diversity. Our method formulates the reranking problem as an optimization of a utility function that jointly considers relevance and diversity. Our main contribution is the replacement of the unsupervised definition of relevance that is commonly used in this formulation with a supervised classification model that strives to capture a query and application-specific notion of relevance. This model provides more accurate relevance scores that lead to significantly improved diversification performance. Furthermore, we propose a stacking-type ensemble learning approach that allows combining multiple features in a principled way when computing the relevance of an image. An empirical evaluation carried out on the datasets of the MediaEval 2013 and 2014 "Retrieving Diverse Social Images" (RDSI) benchmarks confirms the superior performance of the proposed method compared to other participating systems as well as a state-of-the-art, unsupervised reranking method.</p>
<p><strong>Data</strong></p>
<p>We make available (<a href="http://mklab.iti.gr/datasets/diversity/spyromitros_IDiISvSRS_data.zip">here</a>) the version of the MediaEval 2014 Retrieving Diverse Social Images dataset that we used in our experiments. In particular, we provide the following data, separately for the development and the test set of the collection:</p>
<ul>
	<li>9 alternative relevance-based orderings (along with the corresponding relevance scores) of the images of&nbsp;each query location. These orderings are obtained by applying the 3 variants of the sMMR method (sMMR<sub>a</sub>,&nbsp;sMMR<sub>q</sub>,&nbsp;sMMR<sub>aq w=1000</sub>) as described in section 5&nbsp;of the paper, using 3 different features (vlad, cnn, bow), again as described in section 5 of&nbsp;the paper. The format of the files is the same as the one of the submission files that were asked from the participants of the task.</li>
	<li>The vlad, cnn and bow features for all images of the collection (both the location images and the wikipedia images). The data files follow the same structure as the ones provided by the organizers of the task for other types of features.</li>
</ul>
<p>The data can be used to reproduce the experimental results presented in the paper as well as to try new methodologies based on the provided image features and relevance scores.</p>
<p><strong>Citation</strong></p>
<p>If you use the dataset in your research, please cite the following paper:</p>
<p>Eleftherios Spyromitros-Xioufis, Symeon Papadopoulos, Alexandru Lucian Ginsca, Adrian Popescu, Yiannis Kompatsiaris, and Ioannis Vlahavas. 2015.&nbsp;<a href="http://dl.acm.org/citation.cfm?id=2749334">Improving Diversity in Image Search via Supervised Relevance Scoring</a>. In Proceedings of the 5th ACM on International Conference on Multimedia Retrieval (ICMR '15). ACM, New York, NY, USA, 323-330. DOI: https://doi.org/10.1145/2671188.2749334</p>
<p><strong>Contact</strong></p>
<p>In case you have any questions about the dataset you can contact:</p>
<ul>
	<li>Eleftherios Spyromitros-Xioufis (espyromi@iti.gr)</li>
	<li>Symeon Papadopoulos (papadop@iti.gr)&nbsp;</li>
</ul>
<div>&nbsp;</div>
<p>&nbsp;</p>
<p>&nbsp;</p>
