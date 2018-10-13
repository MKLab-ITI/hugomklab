---
excerpt: "LinkedTV's personalisation and contextualisation services involve capturing,
  learning and creating semantic user profiles implicitly based on the user's online
  behaviour with networked media"
types: results
tags:
- tool
- module
images: []
layout: results
title: Linked Profiler
date: '2013-09-02T11:58:28+03:00'
---
<p>LinkedTV's personalisation and contextualisation services involve capturing, learning and creating semantic user profiles implicitly based on the user's online behaviour with networked media. To this end, CERTH-ITI has implented services for managing and learning user interests and wrapping intra- and extra-CERTH-developed tools under a semantic profile construction workflow.</p>
<p>These tools are bundled under a modelling component API that handles storage and update of the profile and provision to all other parts of the LinkedTV personalisation workflow, namely <strong>Linked Profiler</strong>.</p>
<p><strong>Jump to:</strong></p>
<p><a href="#descr">Description</a></p>
<p style="margin-left: 40px;"><a href="#lumowrapper">LUMO wrapper</a></p>
<p style="margin-left: 40px;"><a href="#simplelearner">Simple Learner</a></p>
<p style="margin-left: 40px;"><a href="#profileconstruction">LinkedTV user profiles</a></p>
<p><a href="#profile api">Linked Profiler REST API</a></p>
<p><a href="#ann api">Additional content profiling services &amp; REST API</a></p>
<p><a href="#Downloads">Downloads</a></p>
<p><a href="#contacts">Contacts</a></p>
<p>&nbsp;</p>
<div style="page-break-after: always;"><span style="display: none;">&nbsp;</span></div>
<h2>Description<a name="descr"></a></h2>
<p><strong>Linked Profiler</strong> is responsible for receiving input by captured or explicitly declared user interests, for incorporating and handling cooperation among all preference capturing and learning tools within the LinkedTV personalisation and contextualisation task and that ultimately produces a fuzzy semantic user profile that can be received as input by the LinkedTV filtering tools.</p>
<p>Two subcomponents developed by CERTH-ITI are incorporated in the Linked Profiler:</p>
<ol>
	<li><strong>LUMO wrapper</strong>, which unifies the semantic description of captured user preferences under a common vocabulary.</li>
	<li><strong>Simple Learner</strong>, which is responsible for learning a user profile over time and content consumption.</li>
</ol>
<p style="text-align: center;"><a href="http://mklab.iti.gr/linkedtv/files/linked_profiler.png"><img alt="" src=" http://mklab.iti.gr/linkedtv/files/linked_profiler.png" style="width: 500px; height: 266px;"></a></p>
<p style="text-align: center;"><strong>The Linked Profiler workflow </strong></p>
<p><em>Association rules mining</em> is an extra-CERTH-ITI component wrapped into the workflow via Linked Profiler.<strong> </strong></p>
<p><em>User information capturing</em> and<em> Filtering</em> are processes outside the Linked Profiler API and are not part of the description of the services presented here, but are only illustrated as indicated input and output.</p>
<p style="margin-left: 40px;">However, <em>Filtering</em> can be achieved via the CERTH-ITI developed tool <a href="http://mklab.iti.gr/project/LiFR">LiFR</a>, among other solutions.</p>
<p>The Linked Profiler is in particular:</p>
<ul>
	<li>responsible for the communication among all preference reception, transormation and learning components,</li>
	<li>responsible for the production of the final semantic user profile.</li>
</ul>
<h3>LUMO wrapper<a name="lumowrapper"></a></h3>
<p>Within LinkedTV, multimedia content is segmented into spatio-temporal fragments, accompanied by metadata stemming from several analysis services within the LinkedTV pipeline. Among this metadata, semantic annotation of <a href="http://www.w3.org/TR/media-frags/">media fragments</a>, describing 'what this fragment is about' may be retrieved. The content analysis tools provide this description into a plurality of <a href="http://en.wikipedia.org/wiki/Linked_data">LOD</a> vocabularies, in the interest of efficient, complete and standardized disambiguation and linking of media fragments.</p>
<p>However, in the interest of more efficient personalisation services, the hetereogenity of content annotation imposed by this variety of descriptive vocabularies, the lack of user-pertinent semantics in vocabularies of a more general purpose, the overflow of information unrelated to a user-centric perspective and the imperfection in the structure and semantics of often user-contributed vocabularies have lead to the need of expressing user preferences in a homogeneous, user-centric reference knowledge base. This KB, namely <a href="http://mklab.iti.gr/project/lumo">LUMO</a>, aims to cover all information pertinent to user in the networked media domain in a uniform, lightweight and formal ontological vocabulary.</p>
<p>To this end, information about user preferences, captured implicitly through his interaction with the content on the LinkedTV platform and based on the content's semantic description is tranformed from this LOD-based annotation into LUMO via the <em><strong>LUMO wrapper</strong></em> component. Through this transformation, uniformly expressed preferences are passed onto the profile learning modules, thus also minimizing the concept space and maintaining the profiles more cohesive and lightweight.</p>
<h3>Simple Learner<a name="simplelearner"></a></h3>
<p>Simple Learner is a baseline profile learning component that adds new preferences (i.e. concepts) to the user profile, weighted based on the interest shown by the user in a given content consumption session. Given this interest, it is able to manage and communicate both captured interests and disinterests.</p>
<p>The learning stage consists of updating the interest weights of existing preferences according to their frequency of appearance in the user's transaction history and the age of the preference (time decay factor).</p>
<p>Simple Learner can also provide an intermediate output of JSON-formatted preferences, before these are coupled with mined association rules (extra-CERTH-ITI component in the Linked Profiler workflow) and serialised in the ontological user profile. This intermediate (called "plain") profile provides an entry per user preference along with its attributes in the user's transaction history of the form:</p>
<p><big><code>"timestamp":{last timestamp that the concept was consumed},"concept":{LUMO-based concept name},"aggregated weight":{sum of interest across all user sessions for this concept},"frequency":{times that concept was accessed},"positive":{TRUE if interest/FALSE if disinterest}</code></big></p>
<h3>Semantic user profile construction<a name="profileconstruction"></a></h3>
<p>The user profile produced is expressed in a variant of the <a href="http://dl.kr.org/dl97/krss.ps">KRSS</a> ontological formalization for two reasons:</p>
<ol>
	<li>The expressivity of the user profile is much richer than a list of weighted concepts and as such can only be expressed in an ontological formalization - rather than a more simple web standard such as <a href="http://JSON">JSON</a>.</li>
	<li>KRSS is significantly more lighweight than other known ontological formalizations/standards (<a href="http://www.w3.org/TR/owl-features/%E2%80%8E">OWL</a>, <a href="http://www.w3.org/RDF/">RDF</a>) and as such accomodates storage and management of ontological profiles much more efficiently.</li>
</ol>
<p>To see details of the supported syntax, please refer to the <a href="http://mklab.iti.gr/project/f-pocketKRHyper#semantics">LiFR supported syntax</a>.</p>
<h4>Example<a name="example"></a></h4>
<p>The example illustrates the contextual profile of user "<strong>Ralph</strong>". The <em>persona specifications</em> are:</p>
<p>Ralph really likes the <strong>band </strong><b>Silbermond</b> and their music, so when content around Silbermong shows on the TV he frequently browses through related content in the RBB broadcast archives or searches the web to find out more about the band. However, he does <b>not</b> care for lengthy <b>interviews</b>.</p>
<p>Other main<em> interests </em>are: <strong>crafts</strong>, <strong>weather</strong>, <strong>local</strong> (he is from <strong>Bradenburg</strong>) <strong>sport clubs</strong> when he is in town, <strong>athletes</strong> in the <strong>Olympics</strong></p>
<p>Other main <em>disinterests </em>are: <strong>politics</strong></p>
<p>Current <em>contextual facts</em> are: <strong>His location</strong> is <strong>Bradenburg</strong> by a confidence &gt;= 0.85</p>
<p>KRSS Ralph profile:</p>
<pre><code>(IMPLIES (SOME has_interest (OR profsubconcept1 inst_silbermond profsubconcept2 crafting weather)) ralph)
(IMPLIES (AND (SOME inRule sports_club) (SOME inRule inst_bradenburg)) profsubconcept1)
(IMPLIES inst_bradenburg user_location)
(IMPLIES inst_silbermond band)
(IMPLIES (AND (SOME inRule olympics) (SOME inRule athlete)) profsubconcept2)
(IMPLIES (SOME has_interest (OR politics interview)) ralph_dis)
(DISJOINT ralph ralph_dis)
(WEIGHT profsubconcept1 0.76)
(WEIGHT inst_bradenburg 0.85)
(WEIGHT inst_silbermond 0.82)
(WEIGHT profsubconcept2 0.51)
(WEIGHT crafting 0.68)
(WEIGHT weather 0.54)
(INSTANCE bradenburg inst_bradenburg <code>&gt;= 0.85</code>)
(INSTANCE silbermond <code>inst_silbermond</code> <code><code>&lt; -1.0</code></code>)
(RELATED rule bradenburg inRule)
(RELATED content bradenburg has_interest)
(RELATED content sibermond has_interest)
</code></pre>
<p><em>Note:</em> Silbermond and Bradenburg are individiduals (most specific entities) and as such they don't belong at the schema level of the reference ontology. To add specific entities as preferences in the user profile, we manufacture a concept "inst_{individual name}", weighteed by the degree of preference, and we extend the TBox with this knowledge by appending it as a subclass of the most specific type that the individual would instantiate in our reference TBox (ontology).</p>
<p>So what would have been (INSTANCE silbermond band) now becomes (IMPLIES inst_silbermond band), (WEIGHT inst_silbermond 0.82), (INSTANCE silbermond inst_silbermond &lt; -1.0).</p>
<p>In the employed LiFR reasoner, a concept assertion of an individual belonging to a concept is essentially non-existent in the KB unless it has a membership degree &gt;=0. A valid concept assertion in our KB will be derived either from (a) contextual facts (the LinkedTV platform has determined that the current user context is this entity), or (b) content annotation facts (a content item candidate for recommendation is about this entity).</p>
<div style="page-break-after: always;"><span style="display: none;">&nbsp;</span></div>
<h2>Linked Profiler REST API<a name="profile api"></a></h2>
<p>Linked Profiler and its subcomponents are supported by a REST API which gives access to services for retrieving and uploading user information on the profiling server. The API is currently hosted on a CERTH-ITI server (base URI: <a href="http://multimedia.iti.gr/api/"><span class="external free ext">http://multimedia.iti.gr/api/</span></a>).</p>
<h3><span class="mw-headline" id="GET_all_profiles_available">GET all profiles available </span></h3>
<p>(For internal use only) Retrieves a list of all user ids available on the server.</p>
<p><b>GET /api/profiles</b></p>
<ul>
	<li>Description: GET /api/profiles</li>
	<li>HTTP method: GET</li>
	<li>Content-Type: application/json</li>
	<li>URI: <a class="external free" href="http://160.40.50.224:8182/api/profiles" rel="nofollow">http://</a><a class="external free ext" href="http://160.40.50.224:8182/api/content_filtering?uid=%7Buid%7D" rel="nofollow" target="_blank">multimedia.iti.gr</a><a class="external free" href="http://160.40.50.224:8182/api/profiles" rel="nofollow">/api/profiles</a></li>
	<li>Example of response:
		<pre><code>{
   "[{"ralph"}]",
   "[{"ralph_context"}]",
   "[{"silbermond_all_content"}]"
}
</code></pre>
	</li>
</ul>
<h3>GET a KRSS user profile</h3>
<p>Receives a given user profile from the server in the KRSS format. This is the final export of Linked Profiler, incorporating a learned model through both Simple Learner and EasyMiner.</p>
<p><b>GET /api/KRSS_profile?uid={uid}</b></p>
<ul>
	<li>Description: GET /api/KRSS_profile?uid={uid}</li>
	<li>HTTP method: GET</li>
	<li>Content-Type: application/json</li>
	<li>URI: <a href="http://multimedia.iti.gr/api/KRSS_profile?uid={uid}"><span class="external free">http://</span><span class="external free ext">multimedia.iti.gr</span><span class="external free">/api/KRSS_profile?uid={uid}</span></a></li>
	<li>Example of response:</li>
</ul>
<pre><code>
{Profile:
(IMPLIES (SOME has_interest (OR profsubconcept1 inst_silbermond profsubconcept2 crafting weather)) ralph)
(IMPLIES (AND (SOME inRule sports_club) (SOME inRule inst_bradenburg)) profsubconcept1)
(IMPLIES inst_bradenburg user_location)
(IMPLIES inst_silbermond band)
(IMPLIES (AND (SOME inRule olympics) (SOME inRule athlete)) profsubconcept2)
(IMPLIES (SOME has_interest (OR politics interview)) ralph_dis)
(DISJOINT ralph ralph_dis)
(WEIGHT profsubconcept1 0.76)
(WEIGHT inst_bradenburg 0.85)
(WEIGHT inst_silbermond 0.82)
(WEIGHT profsubconcept2 0.51)
(WEIGHT crafting 0.68)
(WEIGHT weather 0.54)
(INSTANCE bradenburg inst_bradenburg &gt;= 0.85)
(INSTANCE silbermond <code>inst_silbermond</code> <code>&lt; -1.0</code>)
(RELATED rule bradenburg inRule)
(RELATED content bradenburg has_interest)
(RELATED content sibermond has_interest)
}
</code></pre>
<h3>G<span class="mw-headline" id="GET_a_plain_user_profile">ET a plain user profile </span></h3>
<p>Receives a given user profile from the server in its plain pre-ontological form (i.e. from <a href="#simplelearner">Simple Learner</a>)</p>
<p><b>GET /api/plain_profile?uid={uid}</b></p>
<ul>
	<li>Description: GET /api/plain_profile?uid={uid}</li>
	<li>HTTP method: GET</li>
	<li>Content-Type: application/json</li>
	<li>URI: <a href="http://multimedia.iti.gr/api/plain_profile?uid={uid}"><span class="external free">http://multimedia.iti.gr/api/plain_profile?uid={uid}</span></a></li>
	<li>Example of response:</li>
</ul>
<pre><code>{
</code>"[{"timestamp":"1.22943E+12","concept":"silbermond:band","aggregated weight":"22.8682","frequency":"40","positive":"TRUE"}]",
"[{"timestamp":"1.22943E+12","concept":"bradenburg:user_location","aggregated weight":"14.2667","frequency":"28","positive":"TRUE"}]",
"[{"timestamp":"1.22943E+12","concept":"profsubconcept1","aggregated weight":"12.2092","frequency":"26","positive":"TRUE"}]",
"[{"timestamp":"1.22943E+12","concept":"profsubconcept2","aggregated weight":"11.3937","frequency":"26","positive":"TRUE"}]",
"[{"timestamp":"1.22943E+12","concept":"crafting","aggregated weight":"10.9337","frequency":"32","positive":"TRUE"}]",
"[{"timestamp":"1.22943E+12","concept":"weather","aggregated weight":"10.9213","frequency":"19","positive":"TRUE"}]",
"[{"timestamp":"1.22942E+12","concept":"politics","aggregated weight":"10","frequency":"10","positive":"FALSE"}]",
"[{"timestamp":"1.22943E+12","concept":"interview","aggregated weight":"9.2095","frequency":"12","positive":"FALSE"}]",
"[{"timestamp":"1.22942E+12","concept":"profsubconcept3","aggregated weight":"8.2045","frequency":"10","positive":"FALSE"}]"<code>
}
</code></pre>
<p><br>
	Note:</p>
<p>Concepts of the form “<em>profsubconcept</em>#”: are pointers to Association Rules. These pointers will help retrieve learned association rules to be transverted onto the final ontological user profile.</p>
<h3>POST a profile on the server</h3>
<p><b>POST /api/upload_profile</b></p>
<ul>
	<li>Description: POST /api/upload_profile</li>
	<li>HTTP method: POST</li>
	<li>Content-Type: text/plain</li>
	<li>URI: <a class="external free" href="http://multimedia.iti.gr/api/upload_profile?uid=%7Buid%7D" rel="nofollow">http://multimedia.iti.gr/api/upload_profile?uid={uid}</a></li>
	<li>Requisite:
		<ul>
			<li>a .txt file containing a profile in the KRSS format (e.g. <a href="#example">profile example</a>)</li>
			<li>The KRSS profile includes an implication axiom where a rule (the interests) imply the profile-concept (e.g. in <a href="#example">profile example</a>, the concept "<em>ralph</em>". The name of the uploaded file must be the same as this profile-concept.</li>
		</ul>
	</li>
	<li>CURL command:</li>
</ul>
<pre><code>curl -i -X POST --data-binary @{uid}.txt <a class="external free" href="http://multimedia.iti/api/upload_profile?uid=%7Buid%7D" rel="nofollow">http://multimedia.iti/api/upload_profile?uid={uid}</a></code></pre>
<ul>
	<li>Result:
		<ul>
			<li>Uploads the selected profile on the server</li>
		</ul>
	</li>
	<li><b>Note!</b> Make sure you notice the argument you give. If you change the argument to "cid" instead if "uid", this call will upload a content annotation profile instead of a user profile (see below).</li>
</ul>
<p>&nbsp;</p>
<div style="page-break-after: always;"><span style="display: none;">&nbsp;</span></div>
<h2>Additional content profiling services &amp; REST API<a name="ann api"></a></h2>
<p>In addition to providing access to the creation, overview and management of semantic user profiles, the modules incorporated within Linked Profiler can also be used to transform semantic content descriptions from LOD to LUMO, expressed again in the KRSS format, in the interest of having a homogenized set of recommendation items, suitable for fast and efficient content filtering via the CERTH-ITI <a href="http://mklab.iti.gr/project/LiFR">LiFR</a> reasoner.&nbsp;</p>
<h4>Example<a name="exampleann"></a></h4>
<pre><code>(IMPLIES (SOME offers (AND inst_silbermond video interview)) silbermond_juergen)
(IMPLIES inst_silbermond band)
(INSTANCE silbermond inst_silbermond &gt;= 0.9)
(INSTANCE vi_1 video &gt;= 0.99)
(INSTANCE in_1 interview &gt;= 0.69)
(RELATED content silbermond offers)
(RELATED content vi_1 offers)
(RELATED content in_1 offers)
(RELATED silbermond content hastopic)
</code></pre>
<p>Where <em><code>silbermond_juergen</code></em> is a content identifier pseudo-concept, pointing to the particular content item (media fragment id), used to retrieve the fragment if it will be recommended.</p>
<h2>Content annotation REST API</h2>
<p>REST services available for producing, managing and accessing content annotation in the KRSS format</p>
<h3>Translation REST API - TBD</h3>
<h3><span class="mw-headline" id="GET_all_annotated_content_available">GET all annotated content available </span></h3>
<p>(For internal use only) Retrieves a list of all annotated content ids available on the server for marchmaking.</p>
<p><b>GET /api/KRSS_content_annotation_files</b></p>
<ul>
	<li>Description: GET /api/KRSS_content_annotation_files</li>
	<li>HTTP method: GET</li>
	<li>Content-Type: application/json</li>
	<li>URI: <a href="http://multimedia.iti.gr/api/KRSS_content_annotation_files"><span class="external free">http://multimedia.iti.gr/api/KRSS_content_annotation_files</span></a></li>
	<li>Example of response:</li>
</ul>
<pre><code> {
   "[{"stilbruch_20120322_silber_m"}]",
   "[{"www_silbermond_de"}]",
   "[{"www_silbermond_de2"}]",
   "[{"radioberlin_silbermond"}]",
   "[{"radioberlin_silbermond_eine"}]",
   "[{"silbermond"}]",
   "[{"silbermondclubconzert"}]",
   "[{"silbermond_juergen"}]",
   "[{"silbermond_seed_content_chapter"}]"
}
</code></pre>
<h3>G<span class="mw-headline" id="GET_a_KRSS_content_profile">ET a KRSS content profile </span></h3>
<p>Receives a given content profile from the server in the KRSS format. This is the input for LiFR's content matching service and will be the set of related content returned by WP2.</p>
<p><b>GET /api/KRSS_content_annotation?cid={cid}</b></p>
<ul>
	<li>Description: GET /api/KRSS_content_annotation?cid={cid}</li>
	<li>HTTP method: GET</li>
	<li>Content-Type: application/json</li>
	<li>URI: <a href="http://multimedia.iti.gr/api/KRSS_content_annotation?cid={cid}"><span class="external free">http://multimedia.iti.gr/api/KRSS_content_annotation?cid={cid}</span></a></li>
	<li>Example of response:</li>
</ul>
<pre><code>{KRSS_content_annotation:
(IMPLIES (SOME offers (AND inst_silbermond video interview)) silbermond_juergen)
(IMPLIES inst_silbermond band)
(INSTANCE silbermond inst_silbermond &gt;= 0.9)
(INSTANCE vi_1 video &gt;= 0.99)
(INSTANCE in_1 interview &gt;= 0.69)
(RELATED content silbermond offers)
(RELATED content vi_1 offers)
(RELATED content in_1 offers)
(RELATED silbermond content hastopic)
}
</code></pre>
<h3>P<span class="mw-headline" id="PUT_a_KRSS_annotation_profile_on_the_server">OST a KRSS annotation profile on the server </span></h3>
<p><b>POST /api/upload_content_annotation</b></p>
<ul>
	<li>Description: POST /api/upload_content_annotation</li>
	<li>HTTP method: POST</li>
	<li>Content-Type: text/plain</li>
	<li>URI: <a class="external free" href="http://multimedia.iti.gr/api/upload_profile?cid=%7Bcid%7D" rel="nofollow">http://multimedia.iti.gr/api/upload_profile?cid={cid}</a></li>
	<li>Requisite:
		<ul>
			<li>a .txt file containing a the annotation of the content item in the KRSS format (e.g. <a href="#exampleann">content profile example</a>)</li>
			<li>The KRSS profile includes an implication axiom where a rule (a conjunction of the concepts annotating the content) imply the profile-concept. The name of the uploaded file must be the same as this profile-concept (e.g. in <a href="http://mklab.iti.gr/#exampleann">content profile example</a>, the concept "silbermond_juergen").</li>
		</ul>
	</li>
	<li>CURL command:</li>
</ul>
<pre><code>curl -i -X POST --data-binary @{cid}.txt <a class="external free" href="http://multimedia.iti/api/upload_profile?cid=%7Bcid%7D" rel="nofollow">http://multimedia.iti/api/upload_profile?cid={cid}</a></code></pre>
<ul>
	<li>Result:
		<ul>
			<li>Uploads the selected profile on the server</li>
		</ul>
	</li>
	<li><b>Note!</b> Make sure you notice the argument you give. If you change the argument to "uid" instead if "cid", this call will upload a user profile instead of a content annotation profile (see above).</li>
</ul>
<p>&nbsp;</p>
<div style="page-break-after: always;"><span style="display: none;">&nbsp;</span></div>
<h2><a name="Downloads">Downloads&nbsp;</a></h2>
<p>Linked Profiler is an open source software, distributed under the <a href="http://www.gnu.org/licenses/lgpl-3.0.en.html">GNU LGPL</a> license. You can download the source code and complementary information from the links below. &nbsp;</p>
<p><a href="http://mklab.iti.gr/images/new/LinkedProfiler_src.tar.gz">The Linked Profiler source code</a>&nbsp;(tar.gz). Includes a copy of the license.</p>
<p><a href="http://mklab.iti.gr/images/new/LinkedProfiler_doc.tar.gz">The Linked Profiler documentation</a> files&nbsp;(tar.gz)</p>
<p><a href="http://mklab.iti.gr/images/new/LinkedProfiler_material.tar.gz">Useful materials</a> (tar.gz). Includes an example user profile, a copy of a version of the <a href="http://mklab.iti.gr/project/lumo">LUMO ontology</a> and accompanying LUMO mappings (in a <a href="http://franz.com/agraph/racer/krss-spec.pdf">KRSS</a>-variant syntax) and a copy of a version of the <a href="http://mklab.iti.gr/project/LiFR">LiFR reasoner</a> library.</p>
<p><em>Disclaimer: Currently the development of Linked Profiler has ceased and no support in bug tracking, versioning (to comply with newer versions of dependent components such as the GAIN user tracking and preference learning web service), or further&nbsp;requests can be provided. &nbsp;&nbsp;</em></p>
<div style="page-break-after: always;"><span style="display: none;">&nbsp;</span></div>
<h2>Contacts&nbsp;<a name="contacts"></a></h2>
<p><em>For Linked Profiler related issues, please contact dorothea [at] iti [dot] gr.</em></p>
<p><em>For LinkedTV related issues, please contact bmezaris [at] iti [dot] gr.</em></p>
