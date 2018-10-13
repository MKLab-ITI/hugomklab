---
excerpt: LiFR, previously known as f-PocketKRHyper after the crisp reasoner it has extended'
types: results
tags:
- tool
- module
- utility
images: []
layout: results
title: LiFR
date: '2014-05-12T14:53:20+03:00'
---
<p><strong>LiFR, </strong>previously known as <em>f-PocketKRHyper</em> after the crisp reasoner it has extended, is a <strong>Li</strong>ghweight <strong>F</strong>uzzy semantic <strong>R</strong>easoner, which for the purposes of the <a href="http://www.linkedtv.eu/">LinkedTV</a> EU project is employed and extended to perform content and concept filtering based on semantic descriptions of a user profile and content items. It is released under the <a href="http://www.gnu.org/licenses/lgpl.html">GNU LGPL</a>.</p>
<p><strong>Jump to:</strong></p>
<p><a href="#description">Description</a></p>
<p style="margin-left: 40px;"><a href="#semantics">LiFR Semantics and Syntax</a></p>
<p style="margin-left: 40px;"><a href="#ltv-services">LiFR Services in LinkedTV</a></p>
<p style="margin-left: 40px;"><a href="#future">Future Extensions</a></p>
<p style="margin-left: 40px;"><a href="#demo">LiFR in LinkedTV demonstrator</a></p>
<p><a href="#restapi">LinkedTV concept and content filtering REST API</a></p>
<p><a href="#downloads">Downloads</a></p>
<p><a href="#contacts">Contacts</a></p>
<p>&nbsp;</p>
<div style="page-break-after: always;"><span style="display: none;">&nbsp;</span></div>
<h2>Description<a name="description"></a></h2>
<p>The algorithmic foundation of LiFR lies in the crisp reasoner it has extended: the <a href="http://ceur-ws.org/Vol-189/submission_36.pdf">Pocket KRHyper</a> mobile reasoner. Thus it is a first-order model generating reasoner implementing the <a href="http://link.springer.com/chapter/10.1007%2F3-540-69778-0_14">hyper-tableaux calculus</a>. DL reasoning in Pocket KRHyper is performed through translating DLs axioms to ﬁrst order clauses, as portrayed in the translation primitives of Pocket KRHyper. The original <a href="http://arxiv.org/pdf/1201.4089.pdf">Description Logic (DL)</a> interface provided by Pocket KRHyper was extended to support added semantics and fuzzy operators’ transformation into the native ﬁrst order clausal implementation.&nbsp;</p>
<p>LiFR has extended Pocket KRHyper to fuzziness and has made improvements on the original implementation efficiency-wise and with respect to disjunction handling. The first extension within CERTH, named then f-PocketKRHyper, was a J2ME application like its crisp predecessor. Since then, it was transformed to JavaSE with an interest in rendering it capable of multi-platform implementations, while maintaining the original implementation's principles of a lightweight and efficient algorithm, capable of performing reasoning services in limited resource devices, such as smartphones, tablets, set-top boxes etc.</p>
<p>The general <em><strong>inferencing </strong></em><em><b>services</b> </em>provided by LiFR are:</p>
<ul>
	<li>Satisfiability checking</li>
	<li>Subsumption checking</li>
	<li>Fuzzy entailment</li>
	<li>GLB (greatest lower bound) calculation</li>
	<li>Global GLB calculation</li>
</ul>
<!--<p>The supported <b>semantics</b> can be found <a href="http://mklab.iti.gr/linkedtv/files/F-pocketKRHyper_semantics.pdf">here</a>.-->
<p>Extending Pocket KRHyper, LiFR’s <em>default reasoning service</em> consists in the generation of all models that satisfy the input fuzzy knowledge base, thereby providing native support for the computation of the <em>global GLB</em>, i.e the GLB for all combinations of individuals and concepts.</p>
<p><span style="font-size:14px;"><strong>LiFR Semantics and Syntax<a name="semantics"></a></strong></span></p>
<p>LiFR supports fuzzy DLP (<em>f</em>-DLP) semantics, except that as of yet fuzzy assertions are restricted to concepts only, with an added support for weighted concept modifiers, while role assertions are treated as crisp with an imposed membership degree of ≥ 1.0 .</p>
<p><em>f</em>-DLP is the fuzzy extension of <a href="http://www.cs.man.ac.uk/~horrocks/Publications/download/2003/p117-grosof.pdf">DLP</a>, a tractable knowledge representation fragment, closely related to the <a href="http://www.w3.org/TR/owl2-profiles/#OWL_2_RL">OWL 2 RL</a> proﬁle, that combines classical DLs with Logic Programs (LP), thus combining ontologies with rules.&nbsp; The crisp operations intersection, union and implication, are extended to fuzzy sets and performed by t-norm, t-conorm and implication functions respectively. The fuzzy set operations of LiFR follow the operators of <a href="http://www-bisc.cs.berkeley.edu/Zadeh-1965.pdf">Zadeh fuzzy logic</a>.</p>
<p style="text-align: center;"><em><img alt="LiFR Semantics" src="http://mklab.iti.gr/linkedtv/files/LiFR_semantics_noneg.png" style="width: 245px; height: 121px;"></em></p>
<p style="text-align: center;"><span style="font-family:lucida sans unicode,lucida grande,sans-serif;"><strong><em>LiFR Semantics</em></strong></span></p>
<p>LiFR's syntax follows a variant of the <a class="ext" href="http://dl.kr.org/dl97/krss.ps" target="_blank">KRSS</a> ontological notation. The choice of the implementation syntax is two-fold:</p>
<ul>
	<li>It provides comprehensive expressivity enabling extension of the representation to fuzzy operators</li>
	<li>It is signiﬁcantly more lightweight compared to other speciﬁcations (e.g. RDF/XML), thus enhancing the capability of fully supporting reasoning services in resource-constrained devices</li>
</ul>
<p style="text-align: center;"><em><img alt="LiFR syntax" src="http://mklab.iti.gr/linkedtv/files/LiFR_KRSS-variant_syntax_noneg.png" style="width: 220px; height: 226px;"></em></p>
<p style="text-align: center;"><span style="font-family:lucida sans unicode,lucida grande,sans-serif;"><strong><em>LiFR Syntax</em></strong></span></p>
<p>Where <em>C, D </em>are concepts (classes), <em>R, S</em> are roles (object properties), <em>a, b</em> are individuals and <em>d, w</em> <em>∈ [0,1] </em>denote the membership degree of a concept assertion and the modiﬁer weight of a concept respectively. In case of crisp assertions a degree of&nbsp; <em>d ≥ 1.0</em> is imposed and respectively if no weight modifier is defined, a <em>w </em>of<em> 1.0</em> is assumed.</p>
<p>Note that:</p>
<ul>
	<li>A role can be declared with all its properties, e.g. <em>(ROLE R :PARENT P :INVERSE S :TRANSITIVE)</em></li>
	<li>Following DLP semantics, universal and existential restrictions are unilateral, i.e. only <em>∃R.C ⊑ D</em> and <em>C ⊑ ∀R.D</em> are supported.</li>
</ul>
<h3>LiFR services in LinkedTV <a name="ltv-services"></a></h3>
<p>LiFR has been ongoing work of CERTH-ITI through several past projects and for the purposes of LinkedTV it has been extended as a personalised and contextualised recommendation service to enable mainly:</p>
<ul>
	<li>Semantic matching of user profiles to multimedia content.</li>
	<li>Concept filtering via interest propagation over a dedicated personalisation-centric ontology (<a href="http://mklab.iti.gr/project/lumo">LUMO</a>).&nbsp;</li>
</ul>
<p>Several other services have been employed within LinkedTV based on LiFR's basic inferencing services, like mappings retrieval within the <a href="http://mklab.iti.gr/lumo/LUMO_mappings.owl">LUMO mappings ontology</a> and topic detection in semantic user and content profiles based on the <a href="http://mklab.iti.gr/lumo/LUMO.owl">LUMO ontology</a>.</p>
<p>Regarding the main filtering service,&nbsp; by appending information about a user’s preferences, formulated with formal semantics, based on a given domain ontology, LiFR can decide whether a given content item matches the user proﬁle and to what degree, based on the fuzzy annotation metadata that accompany the content item and modiﬁed by the weight indicating the user’s level of preference to a concept.</p>
<p>Implementation of these services include:</p>
<ul>
	<li>Adaptation to the LinkedTV knowledge space and extension to include instances in the user profile (instances were limited to semantic content descriptions).</li>
	<li>Refutation of content or concepts deemed as uninteresting to the given user, based on his profile-incorporated disinterests.</li>
</ul>
<p>To support filtering services, LiFR needs as input a reference domain ontology (within LinkedTV a dedicated ontology was developed to cover the networked media domain, namely <em>LUMO</em>), a semantic user profile and a set of semantic descriptions of content items to be considered for recommendation (the latter only for content filtering). Examples of user profiles and&nbsp; content profiles in the KRSS variant syntax can be found in the supportive tool for semantic user profile construction developed within LinkedTV, <a href="http://mklab.iti.gr/project/linkedtv-profiling-tools">Linked Profiler</a>.</p>
<h3>Future extensions <a name="future"></a></h3>
<p>Additional extensions planned within LinkedTV include the extension of the reasoner's expressivity to cover the entirety of the OWL 2 RL profile and fuzzy role assertions. On the semantic filtering level for LinkedTV, several extensions are considered, like extending concept filtering with an option of a degree decay factor along each propagation step of the interests along the reference knowledge base and/or adding conditionals support in the inferencing logic.</p>
<h3>LiFR in LinkedTV Demonstrator <a name="demo"></a></h3>
<p>A video demonstrator of the concept and content filtering services in the context of LinkedTV can be found <a href="http://www.youtube.com/watch?v=DxZ5bC3Q-Cc">here</a>.</p>
<p>An online demo page, illustrating real-time content and concept filtering in the scope of LinkedTV, as well as topic detection within media content, using the LiFR reasoner, can be found <a href="http://multimedia.iti.gr:8080/reasoner/index.jsp">here</a>.&nbsp;</p>
<div style="page-break-after: always;"><span style="display: none;">&nbsp;</span></div>
<h2>Content and concept filtering REST API<a name="restapi"></a></h2>
<p>LinkedTV content and concept filtering services via semantic reasoner are supported by a REST API, currently hosted on a CERTH-ITI server (base URI: <a href="http://multimedia.iti.gr/api/"><span class="external free">http://multimedia.iti.gr/api/</span></a>).</p>
<h3>Content filtering</h3>
<p>Invokes and returns the results of the process of filtering several content items based on a given user profile, i.e. a list of content items, ranked according to the estimated preference of the given user.</p>
<p><b>GET /api/content_filtering?uid={uid}</b></p>
<ul>
	<li>Description: GET /api/content_filtering?uid={uid}</li>
	<li>HTTP method: GET</li>
	<li>Content-Type: application/json</li>
	<li>URI: <a href="http://multimedia.iti.gr/api/content_filtering?uid={uid}"><span class="external free">http://multimedia.iti.gr/api/content_filtering?uid={uid}</span></a></li>
	<li>Example of response:</li>
</ul>
<pre><code>{
   "[{"Degree":"0.6723999999999999","URL":"www.example.org","cid":"silbermond_seed_content_chapter"}]",
   "[{"Degree":"0.6723999999999999","URL":"www.example.org","cid":"stilbruch_20120322_silber_m"}]",
   "[{"Degree":"0.6723999999999999","URL":"www.example.org","cid":"silbermondclubconzert"}]",
   "[{"Degree":"0.6051599999999999","URL":"www.example.org","cid":"radioberlin_silbermond"}]",
   "[{"Degree":"0.6051599999999999","URL":"www.example.org","cid":"www_silbermond_de"}]",
   "[{"Degree":"0.6051599999999999","URL":"www.example.org","cid":"radioberlin_silbermond_eine"}]"
}

</code></pre>
<h3>Concept filtering</h3>
<p>Invokes and returns the results of the process of retrieving all concepts of interest to a user based on a given profile, i.e. an unranked (at the moment, future implementation will see to ranking it) list of concepts from a dedicated concept space onto which the given user's interests are propagated.</p>
<p><b>GET /api/concept_filtering?uid={uid}</b></p>
<ul>
	<li>Description: GET /api/concept_filtering?uid={uid}</li>
	<li>HTTP method: GET</li>
	<li>Content-Type: application/json</li>
	<li>URI: <a href="http://multimedia.iti.gr/api/content_filtering?uid={uid}"><span class="external free">http://multimedia.iti.gr/api/concept_filtering?uid={uid}</span></a></li>
	<li>Example of response:</li>
</ul>
<p>&nbsp;</p>
<pre><code>{
 [{Degree":1.00,"Concept":"location"}],
 [{Degree":0.82,"Concept":"agent"}],
 [{Degree":1.00,"Concept":"intangible"}],
 [{Degree":0.82,"Concept":"music_organization"}],
 [{Degree":0.76,"Concept":"AND sports_club user_location"}],
 [{Degree":1.00,"Concept":"person"}],
 [{Degree":1.00,"Concept":"sports_club"}],
 [{Degree":0.68,"Concept":"lifestyle_leisure"}],
 [{Degree":0.68,"Concept":"leisure"}],
 [{Degree":1.00,"Concept":"user_dimensions"}],
 [{Degree":1.00,"Concept":"sports_event"}],
 [{Degree":0.68,"Concept":"recreation"}],
 [{Degree":1.00,"Concept":"context_dimensions"}],
 [{Degree":0.51,"Concept":"AND olympics athlete"}],
 [{Degree":1.00,"Concept":"spatio-temporal"}],
 [{Degree":1.00,"Concept":"athlete"}],
 [{Degree":0.68,"Concept":"crafting"}],
 [{Degree":1.00,"Concept":"sports_agent"}],
 [{Degree":0.82,"Concept":"band"}],
 [{Degree":1.00,"Concept":"olympics"}],
 [{Degree":0.68,"Concept":"hobby"}],
 [{Degree":1.00,"Concept":"event"}],
 [{Degree":0.68,"Concept":"topics"}],
 [{Degree":1.00,"Concept":"sports_organization"}],
 [{Degree":1.00,"Concept":"domain_dependent_dimensions"}],
 [{Degree":0.54,"Concept":"weather"}],
 [{Degree":1.00,"Concept":"user_location"}],
 [{Degree":0.82,"Concept":"organization"}],
}
</code>
</pre>
<h2>Downloads <a name="downloads"></a></h2>
<p>To be released soon.</p>
<h2>Contacts <a name="contacts"></a></h2>
<p><em>For LiFR related issues, please contact dorothea [at] iti [dot] gr.</em></p>
<p><em>For LinkedTV related issues, please contact bmezaris [at] iti [dot] gr.</em></p>
