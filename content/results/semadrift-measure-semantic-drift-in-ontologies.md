---
excerpt: 'An active field of research, aiming to identify and measure changes in ontologies across time and versions'
types: results
tags:
- tool
images:
- 6 Results -  Average Stability and ConceptPerConcept Stability.png
- Image 004.png
- Image 008.png
- Image 104.png
layout: results
title: 'SemaDrift: Measure Semantic Drift in Ontologies'
date: '2016-07-27T15:40:08+03:00'
---
<p><strong>Semantic drift</strong> is an active field of research, aiming to identify and measure changes in ontologies across time and versions. It is closely related to ontology evolution. However, practical and widely adopted methods that are directly applicable to Semantic Web constructs have yet to emerge.</p>
<p>SemaDrift is a framework of tools and metrics to measure semantic drift in ontologies across time or versions, using text and structural similarity methods to provide valuable insights. The methods are directly applicable to any ontology originating from any domain of application.</p>
<p>The SemaDrift framework of tools and methods is developed within the <a href="http://pericles-project.eu/">PERICLES FP7 Project</a>.</p>
<h2>SemaDrift Library (API)</h2>
<p>This API written in Java is the core library that processes and parses ontology versions to extract drift metrics. It supports an array of multiple ontology versions and leverages the OWL-API library for parsing. It also provides some utilities to clients, such as to obtain the ontology hierarchies in tree-structures, to eliminate the need of re-processing models.</p>
<p><a data-unsp-sanitized="clean" href="http://mklab.iti.gr/files/SemaDrift%20Library%200.9.zip" type="application/zip; length=30614826">Download here</a></p>
<p><a href="https://github.com/psmert/SemaDrift-Library-API">Get the latest open source version from GitHub</a></p>
<h2>SemaDrift Protégé Plugin</h2>
<p>This plugin provides integration with the Protégé popular ontology creation software, providing a plugin GUI in its environment to calculate drift. It leverages the Java SemaDrift&nbsp;Library to provide drift metrics for two consecutive versions: one open in Protégé and a second ontology of choice. It requires a 4.* version of the Protégé framework.</p>
<p><a data-unsp-sanitized="clean" href="http://mklab.iti.gr/files/SemaDrift%20Protege%20plugin.zip" type="application/zip; length=53154817">Download here</a></p>
<h2>SemaDrift Fx</h2>
<p>This standalone application in the Java Platform is intended for use in Desktop computers, enabling drift measurement between two consecutive ontology versions of choice. It provides a user-friendly GUI for leveraging the SemaDrift&nbsp;Library API.</p>
<p><a data-unsp-sanitized="clean" href="http://mklab.iti.gr/files/SemaDriftFx105_0.zip" type="application/zip; length=53154817">Download here</a></p>
<p><a href="https://github.com/psmert/SemaDriftFx">Get the latest open source version from GitHub</a></p>
<h2>Documentation</h2>
<p><a href="http://mklab.iti.gr/files/SemaDrift%20Protege%20-%20Fx%20Manual%20105_0.pdf">SemaDrift Protege - Fx Manual</a></p>
<h2>Relevant Publications</h2>
<ul>
	<li>Stavropoulos, T.G., Andreadis, S., Kontopoulos, E., Riga, M., Mitzias, P., Kompatsiaris, I.: <a href="https://link.springer.com/chapter/10.1007%2F978-3-319-58694-6_3">The SemaDrift Protégé Plugin to Measure Semantic Drift in Ontologies: Lessons Learned</a>. In: Ciancarini, P., Poggi, F., Horridge, M., Zhao, J., Groza, T., Suarez-Figueroa, M.C., D’Aquin, M., and Presutti, V. (eds.) Knowledge Engineering and Knowledge Management: EKAW 2016 Satellite Events, EKM and Drift-an-LOD, Bologna, Italy, November 19--23, 2016, Revised Selected Papers. pp. 29–39.</li>
	<li>Stavropoulos, T.G., Kontopoulos, E., Meroño-Peñuela, A., Tachos, S., Andreadis, S., Kompatsiaris, I.: <a href="http://ceur-ws.org/Vol-1824/mepdaw_paper_5.pdf">Cross-domain Semantic Drift Measurement in Ontologies Using the SemaDrift Tool and Metrics</a>. In: 3rd Workshop on Managing the Evolution and Preservation of the Data Web (MEPDaW 2017), Portoroz, Slovenia (2017).</li>
	<li>T. G. Stavropoulos, S.Andreadis, E. Kontopoulos, M. Riga, P. Mitzias and I. Kompatsiaris, "<a href="http://event.cwi.nl/drift-a-lod/2016/papers/Drift-a-LOD2016_paper_2.pdf">SemaDrift: A Protégé Plugin for Measuring Semantic Drift in Ontologies</a>", In: Hollink, L., Darányi, S., Meroño Peñuela, A., and Kontopoulos, E. (eds.) 1st International Workshop on Detection, Representation and Management of Concept Drift in Linked Open Data (Drift-a-LOD) in conjunction with the 20th International Conference on Knowledge Engineering and Knowledge Management (EKAW). pp. 34–41. CEUR Workshop Proceedings Vol 1799, Bologna, Italy (2016).</li>
	<li>T. G. Stavropoulos, S.Andreadis, M. Riga, E. Kontopoulos, P. Mitzias and I. Kompatsiaris, "<a href="http://ceur-ws.org/Vol-1695/paper42.pdf">A Framework for Measuring Semantic Drift in Ontologies</a>", In: Martin, M., Cuquet, M., and Folmer, E. (eds.) Joint Proceedings of the Posters and Demos Track of the 12th International Conference on Semantic Systems - SEMANTiCS2016 and the 1st International Workshop on Semantic Change &amp; Evolving Semantics (SuCCESS’16). CEUR Workshop Proceedings Vol 1695, Leipzig, Germany (2016).</li>
</ul>
<h2>Contact</h2>
<ul>
	<li><a href="mailto:athstavr@iti.gr?subject=SemaDrift">Dr. Thanos Stavropoulos</a></li>
	<li><a href="mailto:andreadisst@iti.gr?subject=SemaDrift">Mr. Stelios Andreadis</a></li>
	<li><a href="mailto:skontopo@iti.gr?subject=SemaDrift">Dr. Efstratios Kontopoulos</a></li>
	<li><a href="mailto:ikom@iti.gr?subject=SemaDrift">Dr. Ioannis Kompatsiaris</a></li>
</ul>
