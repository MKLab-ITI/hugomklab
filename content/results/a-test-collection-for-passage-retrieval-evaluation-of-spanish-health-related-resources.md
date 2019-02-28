---
excerpt: 'This dataset was created for evaluating the performance of passage retrieval'
types: results
tags:
- data
images: []
layout: results
title: A Test Collection for Passage Retrieval Evaluation of Spanish Health-Related Resources
date: '2019-01-321T10:51:45+03:00'
---
<p><b>Description</b></p>
<p>This dataset is a new test collection for passage retrieval from health-related Web resources in Spanish. The task being modeled is that of a Spanish-speaking user with information needs on the subjects of "baby care", "vaccination", or "low back pain" in reputable health-related websites in Spanish and the system retrieves relevant short passages. </p>
</p>The test collection contains 10,037 health-related Web documents in Spanish, 37 topics representing complex information needs formulated in a total of 167 natural language questions, and manual relevance assessments of text passages, pooled from multiple systems. </p>
<p><b>Details of the Dataset</b></p>
<p>
For each topic of the dataset we provide:<br/>
1.	The topic id<br/>
2.	The name of the topic (in Spanish)<br/>
3.	The category of the topic<br/>
4.	A short description of the topic (in English)<br/>
5.	A set of natural language questions that are relevant to the topic (in Spanish)<br/>
</p>
<p>
For each document of the dataset we provide:<br/>
1.	The document number serving as its identifier (id)<br/>
2.	The URL of the Web resource corresponding to the specific document<br/>
3.	The resulting HTML content from the scraping procedure performed on the respective Web resource<br/>
4.	The plain text that was finally indexed after processing the HTML content<br/>
</p>
<p>
For each relevance assessment at document level we provide:<br/>
1.	The topic id<br/>
2.	The document id<br/>
3.	Its relevance score (which receives always the value of “1” as we provide only the relevant documents)<br/>
</p>
<p>
For each relevance assessment at passage level we provide: <br/>
1.	The topic id<br/>
2.	The document id<br/>
3.	The starting character index of the relevant passage<br/>
4.	The ending character index of the relevant passage<br/>
5.	Its relevance score (which receives always the value of "1" as we provide only the relevant passages)<br/>
</p>
<p><b>Provided files</b></p>
<p>
The needed files for using the created dataset can be downloaded from <a href="http://mklab.iti.gr/files/PRES_Dataset.rar"><strong>here</strong></a>. After unpacking the compressed file ("PRES_Dataset.rar") a single directory will be generated containing the following files:
<br/>
1.	A JSON file describing the topics<br/>
2.	A JSON file describing the documents<br/>
3.	A "trec_eval" format file providing the relevance assessments at the document level for pooled documents<br/>
4.	A JSON file describing the relevance assessments at passage level for pooled documents<br/>
</p>
<p><b>Copyright</b></p>
<p>TBD</p>
<p><b>Publication</b></p>
<p>If you use this dataset, please cite the following scientific work:<br/>
[1] E. Kamateri, T. Tsikrika, S. Symeonidis, S. Vrochidis, W. Minker and Y. Kompatsiaris, “A test collection for passage retrieval evaluation from health-related resources in Spanish”, 41st European Conference on Information Retrieval (ECIR 2019), 14-18 April 2019, Cologne, Germany
</p>
<p><b>Contact</b></p>
<p>For any queries, please contact:<br/>
ekamater@iti.gr (Eleni Kamateri)<br/>
theodora.tsikrika@iti.gr (Theodora Tsikrika)<br/>
spyridons@iti.gr (Spyridon Symeonidis)<br/>
stefanos@iti.gr (Stefanos Vrochidis)<br/>
</p>
<p><b>Acknowledgements</b></p>
<p>This work is supported by the EU's H2020 KRISTINA project (645012) and the European Regional Development Fund of EU and Greek national funds through the Operational Program Competitiveness, Entrepreneurship and Innovation, under the call RESEARCH-CREATE-INNOVATE for the REA project (T1EDK-00686).</p>

