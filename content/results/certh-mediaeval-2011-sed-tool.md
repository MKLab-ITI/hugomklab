---
excerpt: "Social Event Detection (SED) in tagged photo collections"
types: results
tags:
- tool
- utility
images: []
layout: results
title: CERTH @ MediaEval 2011 SED Tool
date: '2011-09-07T15:26:26+03:00'
---
<p>Social Event Detection (SED) in tagged photo collections</p>
<p><span style="font-size:14px;"><strong>Description</strong></span></p>
<p style="font-family: Arial, Verdana, sans-serif; font-size: 12px; ">This is a Java library implementing the framework presented by CERTH in the <a href="http://www.multimediaeval.org/mediaeval2011/SED2011/">Social Event Detection</a> task at <a href="http://www.multimediaeval.org/mediaeval2011/">MediaEval 2011</a>. It can be used as a competing method for detecting events in large tagged photo collections. In addition, it contains several utility methods for loading the metadata (in the format distributed by the SED task organizers) and computing the performance of the method.</p>
<p style="font-family: Arial, Verdana, sans-serif; font-size: 12px; ">&nbsp;</p>
<p><strong><span style="font-size:14px;">Instructions</span></strong></p>
<p>1. Download the rar archive <a href="http://mklab.iti.gr/files/sed2011_certh.rar">here</a>.</p>
<p>2. Unzip the archive in your Java workspace. A sample class using the library is located in src\test\SubmissionTester.java.</p>
<p>3. Make sure that you include all libraries in the lib folder in your class path.</p>
<p>4. In the data folder there are several data files that are used by the implemented methods as "background" knowledge. You might be interested in tweaking those in order to examine their influence on the performance of the framework (for instance, the tag models used for classification of a photo into cities, the soccer topic and venue).</p>
<p>5. You may extend/override the abstract class SubmissionCreator.java in order to prepare your own solution to the problem of Social Event Detection.</p>
<p>6. You may use the Evaluator.java class in order to compute the performance of your method against a given ground truth.</p>
<p style="font-family: Arial, Verdana, sans-serif; font-size: 12px; ">&nbsp;</p>
<p><span style="font-size:14px;"><strong>Publication</strong></span></p>
<p style="font-family: Arial, Verdana, sans-serif; font-size: 12px; "><font size="2" face="Arial"><span style="font-size: 10pt; line-height: 16px; font-family: Arial; " lang="EN-US">If you make use of this software for your research work, please cite the following paper:</span></font></p>
<p style="font-family: Arial, Verdana, sans-serif; font-size: 12px; "><font size="2" face="Arial"><span style="font-size: 10pt; font-family: Arial; " lang="EN-US">S. Papadopoulos, C. Zigkolis, Y. Kompatsiaris, A. Vakali. “CERTH @ MediaEval 2011 SED Task” In Proceedings of MediaEval 2011 Workshop, Pisa, Italy, 1-2 September 2011</span></font></p>
<p>&nbsp;</p>
<p><span style="font-size:14px;"><strong>License</strong></span></p>
<h3>THIS SOFTWARE IS PROVIDED BY THE AUTHOR "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.</h3>
<p style="font-family: Arial, Verdana, sans-serif; font-size: 12px; ">&nbsp;</p>
<p><span style="font-size:14px;"><strong>Acknowledgements</strong></span></p>
<p style="font-family: Arial, Verdana, sans-serif; font-size: 12px; "><font size="2" face="Arial"><span style="font-size: 10pt; font-family: Arial; " lang="EN-GB">This work was supported by the EU FP7 projects GLOCAL (FP7-248984) and WeKnowIt (FP7-215453).</span></font></p>
<p style="font-family: Arial, Verdana, sans-serif; font-size: 12px; ">&nbsp;</p>
<p><span style="font-size:14px;"><strong>Contact</strong></span></p>
<p style="font-family: Arial, Verdana, sans-serif; font-size: 12px; ">You may contact Symeon Papadopoulos (papadop AT iti DOT gr) for any question or remark you may have with respect to this tool.</p>
