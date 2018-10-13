---
excerpt: 'A fuzzy semantic reasoner employed to perform content and concept filtering based on semantic descriptions
  of a user profile and content items'
types: results
tags:
- tool
- utility
images: []
layout: results
title: f-PocketKRHyper
date: '2013-09-02T12:08:15+03:00'
---
<p><strong>f-PocketKRHyper</strong> is a fuzzy semantic reasoner, which for the purposes of the <a href="http://www.linkedtv.eu/">LinkedTV</a> EU project is employed to perform content and concept filtering based on semantic descriptions of a user profile and content items. It is released under the <a href="http://www.gnu.org/licenses/lgpl.html">GNU LGPL</a>.</p><!--break--><p>&nbsp;</p><p><strong>Jump to:</strong></p><p><a href="#description">Description</a></p><p><a href="#restapi">REST API</a></p><p>&nbsp;</p><div style="page-break-after: always;"><span style="display: none;">&nbsp;</span></div><h2>Description<a name="description"></a></h2><p>The algorithmic foundation of f-PocketKRHyper lies in the crisp reasoner it has extended: the <a href="http://ceur-ws.org/Vol-189/submission_36.pdf">Pocket KRHyper</a> mobile reasoner. Thus it is a first-order model generating reasoner implementing the <a href="http://link.springer.com/chapter/10.1007%2F3-540-69778-0_14">hyper-tableaux calculus</a>. Its expressivity lies within the tractable <a href="http://www.cs.man.ac.uk/~horrocks/Publications/download/2003/p117-grosof.pdf">DLP fragment</a>. f-PocketKRHyper has extended Pocket KRHyper to fuziness and has made improvements on the original implementation efficiency-wise and with respect to disjunction handling. Since its first extension, the original J2ME implementation was transformed back to JavaSE, while maintaining the original implementation&#39;s principles of a lightweight and efficient algorithm, capable of performing reasoning services in limited resource devices.</p><p>Within CERTH it has been extended to fuzziness (along with several other algorithmic optimizations), handling fuzzy concept assertions and weighted concepts. It currently supports:</p><ul><li>Fuzziness in concept assertions. Crisp semantics supported as assertions with degree &ge; 1.</li><li>Crisp role assertions</li><li>Weighted concepts</li></ul><p>The general inferencing <b>services</b> provided by f-PocketKRHyper are:</p><ul><li>Subsumption</li><li>Fuzzy entailment</li></ul><p>The supported <b>semantics</b> can be found <a href="http://mklab.iti.gr/linkedtv/files/F-pocketKRHyper_semantics.pdf">here</a>.</p><h3>f-PocketKRHyper recommendation services in LinkedTV</h3><p>f-PocketKRHyper has been ongoing work of CERTH-ITI through several past projects and for the purposes of LinkedTV it has been extended as a personalised and contextualised recommendation service to enable:</p><ul><li>Semantic matching of user profiles to multimedia content.</li><li>Concept filtering via interest propagation over a dedicated personalisation-centric concept space.&nbsp;</li></ul><p>Implementation of these services include:</p><ul><li>Adaptation to the LinkedTV knowledge space and extension to include instances in the user profile (instances were limited to semantic content descriptions).</li><li>Refutation of content or concepts deemed as uninteresting to the given user, based on his profile-incorporated disinterests.</li></ul><p>To support filtering services, f-PocketKRHyper needs as input a reference knowledge base (within LinkedTV a dedicated ontology was developed to cover the networked media domain, namely <a href="http://mklab.iti.gr/project/lumo">LUMO</a>), a semantic user profile and a set of semantic descriptions of content items to be considered for recommendation (the latter only for content filtering). All the input is expressed in a variant of the <a href="http://dl.kr.org/dl97/krss.ps">KRSS</a> ontological notation. Examples can be found in the supportive tool for semantic user profile construction developed within LinkedTV, namely <a href="http://mklab.iti.gr/project/linkedtv-profiling-tools">Linked Profiler</a>.</p><h3>Future extensions</h3><p>Additional extensions planned within LinkedTV include the extension of the reasoner&#39;s expressivity to cover the entirety of the <a href="http://www.w3.org/TR/owl2-profiles/#OWL_2_RL">OWL 2 RL</a> fragment (an extension of the DLP fragmet to OWL 2 expressivity) and fuzzy role assertions. On the semantic filtering level, concept filtering will be extended with an option of a degree decay factor along each propagation step of the interests along the reference knowledge base.</p><h3>Demonstrator</h3><p>A video demonstrator of the concept and content filtering services can be found <a href="http://www.youtube.com/watch?v=DxZ5bC3Q-Cc">here</a>.</p><p>&nbsp;</p><p>&nbsp;</p><div style="page-break-after: always;"><span style="display: none;">&nbsp;</span></div><h2>Content and concept filtering REST API<a name="restapi"></a></h2><p>LinkedTV content and concept filtering services via semantic reasoner are supported by a REST API, currently hosted on a CERTH-ITI server (base URI: <a class="external free" href="http://160.40.50.224:8182/api/content_filtering?uid=%7Buid%7D" rel="nofollow">http://160.40.50.224:8182/api/</a>) until integrated onto the LinkedTV platform.</p><h3>Content filtering</h3><p>Invokes and returns the results of the process of filtering several content items based on a given user profile, i.e. a list of content items, ranked according to the estimated preference of the given user.</p><p><b>GET /api/content_filtering?uid={uid}</b></p><ul><li>Description: GET /api/content_filtering?uid={uid}</li><li>HTTP method: GET</li><li>Content-Type: application/json</li><li>URI: <a class="external free" href="http://160.40.50.224:8182/api/content_filtering?uid=%7Buid%7D" rel="nofollow">http://160.40.50.224:8182/api/content_filtering?uid={uid}</a></li><li>Example of response:</li></ul>
<pre>
<code>{
   &quot;[{&quot;Degree&quot;:&quot;0.6723999999999999&quot;,&quot;URL&quot;:&quot;www.example.org&quot;,&quot;cid&quot;:&quot;silbermond_seed_content_chapter&quot;}]&quot;,
   &quot;[{&quot;Degree&quot;:&quot;0.6723999999999999&quot;,&quot;URL&quot;:&quot;www.example.org&quot;,&quot;cid&quot;:&quot;stilbruch_20120322_silber_m&quot;}]&quot;,
   &quot;[{&quot;Degree&quot;:&quot;0.6723999999999999&quot;,&quot;URL&quot;:&quot;www.example.org&quot;,&quot;cid&quot;:&quot;silbermondclubconzert&quot;}]&quot;,
   &quot;[{&quot;Degree&quot;:&quot;0.6051599999999999&quot;,&quot;URL&quot;:&quot;www.example.org&quot;,&quot;cid&quot;:&quot;radioberlin_silbermond&quot;}]&quot;,
   &quot;[{&quot;Degree&quot;:&quot;0.6051599999999999&quot;,&quot;URL&quot;:&quot;www.example.org&quot;,&quot;cid&quot;:&quot;www_silbermond_de&quot;}]&quot;,
   &quot;[{&quot;Degree&quot;:&quot;0.6051599999999999&quot;,&quot;URL&quot;:&quot;www.example.org&quot;,&quot;cid&quot;:&quot;radioberlin_silbermond_eine&quot;}]&quot;
}

</code></pre>
<h3>Concept filtering</h3><p>Invokes and returns the results of the process of retrieving all concepts of interest to a user based on a given profile, i.e. an unranked list of concepts from a dedicated concept space onto which the given user&#39;s interests are propagated.</p><p><b>GET /api/concept_filtering?uid={uid}</b></p><ul><li>Description: GET /api/concept_filtering?uid={uid}</li><li>HTTP method: GET</li><li>Content-Type: application/json</li><li>URI: <a class="external free" href="http://160.40.50.224:8182/api/concept_filtering?uid=%7Buid%7D" rel="nofollow">http://160.40.50.224:8182/api/concept_filtering?uid={uid}</a></li><li>Example of response:</li></ul><p>&nbsp;</p>
<pre>
<code>{
[{Degree&quot;:1.00,&quot;Concept&quot;:&quot;location&quot;}],
[{Degree&quot;:0.82,&quot;Concept&quot;:&quot;agent&quot;}],
[{Degree&quot;:1.00,&quot;Concept&quot;:&quot;intangible&quot;}],
[{Degree&quot;:0.82,&quot;Concept&quot;:&quot;music_organization&quot;}],
[{Degree&quot;:0.76,&quot;Concept&quot;:&quot;AND sports_club user_location&quot;}],
[{Degree&quot;:1.00,&quot;Concept&quot;:&quot;person&quot;}],
[{Degree&quot;:1.00,&quot;Concept&quot;:&quot;sports_club&quot;}],
[{Degree&quot;:0.68,&quot;Concept&quot;:&quot;lifestyle_leisure&quot;}],
[{Degree&quot;:0.68,&quot;Concept&quot;:&quot;leisure&quot;}],
[{Degree&quot;:1.00,&quot;Concept&quot;:&quot;user_dimensions&quot;}],
[{Degree&quot;:1.00,&quot;Concept&quot;:&quot;sports_event&quot;}],
[{Degree&quot;:0.68,&quot;Concept&quot;:&quot;recreation&quot;}],
[{Degree&quot;:1.00,&quot;Concept&quot;:&quot;context_dimensions&quot;}],
[{Degree&quot;:0.51,&quot;Concept&quot;:&quot;AND olympics athlete&quot;}],
[{Degree&quot;:1.00,&quot;Concept&quot;:&quot;spatio-temporal&quot;}],
[{Degree&quot;:1.00,&quot;Concept&quot;:&quot;athlete&quot;}],
[{Degree&quot;:0.68,&quot;Concept&quot;:&quot;crafting&quot;}],
[{Degree&quot;:1.00,&quot;Concept&quot;:&quot;sports_agent&quot;}],
[{Degree&quot;:0.82,&quot;Concept&quot;:&quot;band&quot;}],
[{Degree&quot;:1.00,&quot;Concept&quot;:&quot;olympics&quot;}],
[{Degree&quot;:0.68,&quot;Concept&quot;:&quot;hobby&quot;}],
[{Degree&quot;:1.00,&quot;Concept&quot;:&quot;event&quot;}],
[{Degree&quot;:0.68,&quot;Concept&quot;:&quot;topics&quot;}],
[{Degree&quot;:1.00,&quot;Concept&quot;:&quot;sports_organization&quot;}],
[{Degree&quot;:1.00,&quot;Concept&quot;:&quot;domain_dependent_dimensions&quot;}],
[{Degree&quot;:0.54,&quot;Concept&quot;:&quot;weather&quot;}],
[{Degree&quot;:1.00,&quot;Concept&quot;:&quot;user_location&quot;}],
[{Degree&quot;:0.82,&quot;Concept&quot;:&quot;organization&quot;}],
}
</code>
</pre>
<h2>Downloads</h2><p>To be released soon.</p>
