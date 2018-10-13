---
excerpt: 'The LinkedTV User Model Ontology'
types: results
tags:
- ontology
- general
images: []
layout: results
title: LUMO
date: '2013-01-30T23:41:57+02:00'
---
<h2>The LinkedTV User Model Ontology (LUMO)</h2>
<p>LUMO [<a href="http://mklab.iti.gr/lumo/LUMO.owl">owl</a>]<br>
	LUMO_mappings [<a href="http://mklab.iti.gr/lumo/LUMO_mappings.owl">owl</a>]<br>
	LUMO documentation [<a href="http://mklab.iti.gr/lumo/lumo_doc/index.html">html</a>]<br>
	LUMO mappings documentation [<a href="http://mklab.iti.gr/lumo/lumo_mappings_doc/index.html">html</a>]</p>
<p>This work is licensed under a <a href="http://creativecommons.org/licenses/by-sa/3.0/">Creative Commons Attribution-ShareAlike License (version 3.0)</a>. This copyright applies to the LUMO Ontology, the LUMO mappings ontology and accompanying documentation.</p>
<p>Creator and publisher: <a href="http://www.iti.gr/">CERTH-ITI</a></p>
<p><a href="#summary">Summary</a></p>
<p><a href="#overview">Overview</a></p>
<p><a href="#influence">Influence by existing vocabularies</a></p>
<p><a href="#mappings">Mappings to existing vocabularies</a></p>
<p><a href="#contacts">Contacts</a></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<div style="page-break-after: always;"><span style="display: none;">&nbsp;</span></div>
<h2>Summary<a name="summary"></a></h2>
<p>The LUMO ontology is developed within the <a href="http://www.linkedtv.eu/">LinkedTV</a> project to semantically represent user-pertinent information, in order to enable semantic personalization and contextualization (i.e. filtering) of concepts and content in the networked media domain. LUMO is designed as an OWL ontology, with its expressivity restricted to the OWL 2 RL profile, in order to maintain the minimal complexity as per the LinkedTV requirements and address scalability and user privacy issues. LUMO is currently accompanied by a separate <a href="#conneexistingvocabs">mappings</a> ontology, modeling mappings of LUMO to several existing ontologies and vocabularies.</p>
<p>LUMO is published under the <a href="http://data.linkedtv.eu/ontologies/lumo">http://data.linkedtv.eu/ontologies/lumo</a> namespace.</p>
<h3>Status of this document</h3>
<p>The LUMO ontology is currently under engineering. Updates are expected on the current version.</p>
<h2>Overview<a name="overview"></a></h2>
<p>LUMO addresses four major user-pertinent aspects: Context Dimensions, Domain-dependent dimensions, Agents and Spatio-Temporal concepts. The two latter aspects may regard both contextual and domain-dependent aspects of the user and as so are modeled independently on the top of the hierarchy.</p>
<p style="text-align: center;"><img alt="" src="http://mklab.iti.gr/lumo/lumo.jpg" style="width: 430px; height: 320px;"></p>
<p style="text-align: center;"><strong><em><span style="font-family:lucida sans unicode,lucida grande,sans-serif;">The LUMO top hierarchy</span></em></strong></p>
<p>Apart from the taxonomy, LUMO models a number of universal restriction axioms relating concepts via non-taxonomical object properties. In the current version, such axioms are mostly of the type <em>Type ⊑ ∀has(Sub)Topic.Topic</em> and enable inference of topics in both the content’s annotation and in the user pro- ﬁle, since content annotation in LinkedTV does not provide this information. <em>Type</em> corresponds to the type of an entity in the annotation (usually an agent, event, location or object), <em>Topic</em> is subsumed by the <em>Topics</em> concept/category of LUMO and <em>hasSubTopic</em>, <em>hasTopic</em> are roles (object properties), for which it holds <em>hasSubTopic</em> <em>⊑ </em><em>hasTopic</em>.</p>
<p style="text-align: center;"><img alt="" src="http://mklab.iti.gr/linkedtv/files/hasTopic.png" style="width: 480px; height: 169px;"></p>
<p style="text-align: center;"><em><strong>An example of a relation of concept Political_Agent to the topic-concept Politics via the hasTopic relation</strong></em></p>
<p style="text-align: center;">&nbsp;</p>
<div style="page-break-after: always;"><span style="display: none;">&nbsp;</span></div>
<h2>Influence by existing vocabularies<a name="influence"></a></h2>
<p>LUMO engineering aims to model the most relevant entities and semantics from open vocabularies and adapt them to the networked media domain and the needs of the LinkedTV users. This includes adopting, adding new and appropriately discarding domain-extraneous information from relevant established vocabularies, as well as redefining semantics, with respect to leveraging LOD inconsistencies and enhancing coherency and completeness of modeled semantics.</p>
<p>The major existing vocabularies that have inspired and guided the engineering of LUMO are:</p>
<p><strong>GUMO</strong> has guided the design of the top level context and domain-dependent dimensions, while several GUMO contextual dimensions where adopted and adapted to LinkedTV’s platform requirements (including camera-based sensor related concepts). Similarly, some LUMO “Topics” have been modeled to a great extent according to the corresponding GUMO "Topics".</p>
<p>The <strong>IPTC news codes</strong> were the main influence towards modeling the LUMO “Topics” hierarchy. Most upper topic categories were adopted per se and subcategories and concepts related to them where revised and adapted to the topics hierarchy. For instance, several subcategories were created (w.r.t. to also <strong>Wikipedia categories</strong>), while concepts in IPTC that were semantically direct descendants (with the “is-a” relationship) of the “Tangible” and “Intangible” LUMO categories were moved to that sub-hierarchy and related to "Topics" with the "hasTopic" and "hasSubtopic" object properties.</p>
<p><strong>Schema.org</strong> influenced the modeling of the “Agent”, “Location”, “Intangible” and “Tangible” categories. These categories where populated also in correspondence to the<strong> DBPedia schema </strong>and the <strong>NERD ontology</strong>; in a smaller extent they were influenced by several other open vocabularies. Modeling these aspects heavily relied on representing information stemming from content annotation within the LinkedTV platform (for more information, cf. <a href="http://www.linkedtv.eu/research/linking-video-to-web-content/">http://www.linkedtv.eu/research/linking-video-to-web-content/</a>).</p>
<p>&nbsp;</p>
<h2>Mappings to existing vocabularies<a name="mappings"></a></h2>
<p>The current version of LUMO is accompanied by a separate mappings ontology that maps LUMO to existing vocabularies. Mappings were generated automatically via the <a href="http://code.google.com/p/logmap-matcher/">LogMap</a> tool and evaluated and revised manually.</p>
<p>Mappings are detached from the ontology in order to enable user modeling and inferencing (recommendation) to take place in the minimum representative concept space, with regard to scalability and user privacy safeguarding issues. Mappings thus serve a) for interpretation of content annotation and b) as the means to facilitate re-use of the ontology by the Semantic Web.</p>
<p>The LUMO mappings ontology is published under the <a href="http://data.linkedtv.eu/ontologies/lumo_mappings">http://data.linkedtv.eu/ontologies/lumo_mappings</a> namespace.</p>
<p>Currently, mappings are available to the main vocabularies that influenced the engineering of LUMO:</p>
<ul>
	<li><a href="http://wiki.dbpedia.org/Ontology">DBPedia schema</a>&nbsp; (currently with v3.8)</li>
	<li><a href="http://schema.org/docs/schemaorg.owl">schema.org</a></li>
	<li><a href="http://nerd.eurecom.fr/ontology/">NERD ontology</a></li>
	<li><a href="http://webtlab.it.uc3m.es/results/NEWS/subjectcodes.owl">IPTC news codes (as categorized by the WebTLab)</a></li>
	<li><a href="http://www.ubisworld.org/ubisworld/documents/gumo/2.0/gumo.owl">GUMO</a></li>
</ul>
<p>Mappings to other open vocabularies are under consideration and engineering. A future extension of LUMO is planned where fuzzy mappings will be embedded in the annotation of the LUMO entities, along with their semantic similarity, via the “isDescribedBy” LUMO annotation property (cf. <a href="http://www.slideshare.net/linkedtv/linked-tv-d42user-profile-schema-and-profile-capturing">http://www.slideshare.net/linkedtv/linked-tv-d42user-profile-schema-and-profile-capturing</a>).</p>
<p>&nbsp;</p>
<p style="text-align: center;"><img alt="" src="http://mklab.iti.gr/linkedtv/files/animal.png" style="width: 360px; height: 197px;"> <img alt="" src="http://mklab.iti.gr/linkedtv/files/organization.png" style="width: 360px;"></p>
<p style="text-align: center;"><em><strong>Mappings of LUMO concepts Animals and Organization to LOD vocabularies</strong></em></p>
<p style="text-align: center;">&nbsp;</p>
<div style="page-break-after: always;"><span style="display: none;">&nbsp;</span></div>
<h2>Contacts&nbsp;<a name="contacts"></a></h2>
<p><em>For LUMO and LUMO mappings related issues, please contact dorothea [at] iti [dot] gr.</em></p>
<p><em>For LinkedTV related issues, please contact bmezaris [at] iti [dot] gr.</em></p>
