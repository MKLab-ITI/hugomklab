---
excerpt: 'This dataset was created for evaluating the performance of passage retrieval'
types: results
tags:
- data
images: []
layout: results
title: Spanish Passage Retrieval dataset (PRES)
date: '2019-01-321T10:51:45+03:00'
---
<p><b>Description</b></p>
<p>This dataset was created for evaluating the performance of passage retrieval. The task being modeled is that of a Spanish-speaking user with information needs on the subjects of "baby care", "vaccination", or "low back pain" in reputable health-related websites in Spanish and the system retrieves relevant short passages.</p>
</p>The test collection contains 10,037 health-related Web documents in Spanish, 37 topics representing complex information needs formulated in a total of 167 natural language questions, and manual relevance assessments of text passages, pooled from multiple systems.</p>
<p><b>Details of the Test Collection</b></p>
<p>
For each document of the dataset we provide:<br/>
1.	A document number serving as its identifier (id)
2.	Its URL
3.	The resulting HTML content from the scraping procedure
4.	The plain text that was finally indexed
</p>
<p>
For each relevance assessment at passage level we provide: 
1.	The topic id
2.	The document id
3.	The starting character index of the relevant passage
4.	The ending character index of the relevant passage
5.	Its relevance score
</p>
<p><b>Provided files</b></p>
<p>
The needed files for using the created dataset can be downloaded from here(). After unpacking the compressed file ("dataset.zip") a single directory will be generated containing the following files:
&nbsp;
1.	A JSON file describing the topics.
2.	A JSON file describing the documents. 
3.	A “trec_eval” format file providing the relevance assessments at the document level for pooled documents.
4.	A JSON file describing the relevance assessments at passage level for pooled documents. 
</p>
<p><b>Copyright</b></p>
<p>TBD</p>
<p><b>Publication</b></p>
<p>If you use this dataset, please cite the following scientific work:
  &nbsp;
[1] E. Kamateri, T. Tsikrika, S. Symeonidis, S. Vrochidis, W. Minker and Y. Kompatsiaris, “A test collection for passage retrieval evaluation from health-related resources in Spanish”, 41st European Conference on Information Retrieval (ECIR 2019), 14-18 April 2019, Cologne, Germany
</p>
<p><b>Contact</b></p>
<p>For any queries, please contact:
&nbsp;
ekamater@iti.gr (Eleni Kamateri), theodora.tsikrika@iti.gr (Theodora Tsikrika), spyridons@iti.gr (Spyridon Symeonidis), stefanos@iti.gr (Stefanos Vrochidis)
</p>
<p><b>Acknowledgements</b></p>
<p>This work is supported by the EU's H2020 KRISTINA Project (645012) and the European Regional Development Fund of EU and Greek national funds under the call RESEARCH-CREATE-INNOVATE (T1EDK-00686).</p>

