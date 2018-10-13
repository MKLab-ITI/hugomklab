---
excerpt: 'The dataset used in (Tsakalidis et al., 2015) on predicting election results using twitter and polls. The dataset contains the ids of the tweets and the poll data used to build the prediction models'
types: results
tags:
- data
images: []
layout: results
title: EU Elections 2014 Prediction dataset
date: '2015-01-10T18:43:41+02:00'
---
<div><strong>Summary</strong></div>
<div>This is the dataset used in (Tsakalidis et al., 2015) on predicting election results using twitter and polls. The dataset contains the ids of the tweets and the poll data used to build the prediction models. You can download the dataset <a href="http://mklab.iti.gr/files/eu2014_prediction_sup_material.zip#overlay-context=project/eu-elections-2014-prediction-dataset">here</a>.</div>
<div>&nbsp;</div>
<div><strong>Citation</strong></div>
<div>If you use this dataset in your research, please cite the following article:</div>
<div>A. Tsakalidis, S. Papadopoulos, A.I. Cristea, I. Kompatsiaris. "Predicting Elections for Multiple Countries Using Twitter and Polls". IEEE Intelligent Systems (to appear in 2015)</div>
<div><!--break--></div>
<div>&nbsp;</div>
<div><strong>Description</strong></div>
<div>The zip file has the following structure:</div>
<div>&nbsp;</div>
<div><em>Folder tweet_ids:</em></div>
<div>keywords.txt contains the keywords used as inputs tot the Twitter Streaming API to perform the collection. The three csv files contain the ids of the collected tweets.</div>
<div>&nbsp;</div>
<div><em>Folder features_polls:</em></div>
<div>The "polls.ods" file provides the information about the polls that we used during our processing (one sheet per country).</div>
<div>&nbsp;</div>
<div>Every arff file contains the features that we extracted for every country on a daily basis. The attribute corresponding to the poll-based value of every party is indicated by the name of the party. The Twitter-based features are provided in the form of "feature_i", where "feature" corresponds to the Twitter-based feature and "i" is a pointer.&nbsp;</div>
<div>The mapping of parties to this index "i" is the following:</div>
<div>&nbsp;</div>
<div><strong>Germany </strong>("de.arff")&nbsp;</div>
<div>1: CDU/CSU</div>
<div>2: SPD&nbsp;</div>
<div>3: Linke&nbsp;</div>
<div>4: Grunen&nbsp;</div>
<div>5: FDP&nbsp;</div>
<div>6: AfD</div>
<div>&nbsp;</div>
<div><strong>The Netherlands </strong>("nl.arff") &nbsp;</div>
<div>1: PVV&nbsp;</div>
<div>2: VDD&nbsp;</div>
<div>3: D66&nbsp;</div>
<div>4: CDA</div>
<div>5: PvdA</div>
<div>6: SP&nbsp;</div>
<div>7: CU &nbsp;(Notice that since "CU/SGP" was a coalition, the features corresponding to both of these indices --7 and 8-- were used as an input for the prediction of "CU/SGP" voting share)</div>
<div>8: SGP (Notice that since "CU/SGP" was a coalition, the features corresponding to both of these indices --7 and 8-- were used as an input for the prediction of "CU/SGP" voting share)</div>
<div>9: GL</div>
<div>10:50PLUS</div>
<div>11:PvdD</div>
<div>&nbsp;</div>
<div><strong>Greece </strong>("gr.arff")</div>
<div>1: ND&nbsp;</div>
<div>2: SYRIZA</div>
<div>3: Potami</div>
<div>4: XA&nbsp;</div>
<div>5: Elia&nbsp;</div>
<div>6: KKE&nbsp;</div>
<div>7: ANEL&nbsp;</div>
<div>8: DIMAR</div>
<div>&nbsp;</div>
<div>The "lefko" attribute in the case of Greece corresponds to the "blank voters" of the polls and was only presented in the case of Greece. It was not used at all in any experiment (neither pre- nor post-electoral).</div>
<div>&nbsp;</div>
<p>&nbsp;</p>
