---
excerpt: "Trains a model for predicting the performance gain of a bootstrapping process prior to actually applying it using two features; the baseline classifier's maturity and the oracle's reliability"
types: results
tags:
- tool
images: []
layout: results
title: Performance Prediction
date: '2014-01-28T14:11:45+02:00'
---
<p>Trains a model for predicting the performance gain of a bootstrapping process prior to actually applying it using two features; the baseline classifier&#39;s maturity (i.e. how close is the current hyperplane to the optimal) and the oracle&#39;s reliability (i.e. how reliable is the oracle in providing the correct labels of new training data). The code can be downloaded from <a href="https://github.com/ehatzi/PerformancePrediction">github</a> or download directly from <a href="/files/performanceprediction/code.rar">here</a>.</p><p>For a test run download the <a href="/files/performanceprediction/features.rar">features</a> and the <a href="/files/performanceprediction/kernels.rar">kernels</a>. Running the code with these data will reproduce the results of the following paper, as shown in Figure 1.</p><p>Elisavet Chatzilari, Spiros Nikolopoulos, Yiannis Kompatsiaris and Josef Kittler, &ldquo;PERFORMANCE PREDICTION OF BOOTSTRAPPING FOR IMAGE CLASSIFICATION&rdquo;</p>

<p>Figure 1: Actual cumulative performance gain with respect to the number of classifiers enhanced, using the proposed regression model to predict the expected performance gain of each classifier. Comparison with three baselines; a) Random, b) Upper and c) Lower baseline.</p><p style="text-align: center;"><img height="468" src="/files/performanceprediction/fig1.jpg" width="795" /></p><p style="text-align: center;"># of enhanced classifiers</p>
