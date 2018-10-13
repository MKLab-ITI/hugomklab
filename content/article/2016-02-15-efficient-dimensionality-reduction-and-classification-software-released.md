---
excerpt: We just released software (executables and sources) for our accelerated Kernel
  Subclass Discriminant Analysis (AKSDA) method and its combination with SVM classifiers.
  This is an efficient dimensionality reduction and classification method, for very
  high-dimensional data.
types: article
tags: []
images: []
layout: article
title: Efficient dimensionality reduction and classification software released
date: '2016-02-15T12:41:03+02:00'
---
<p>We just released software (executables and sources) for our accelerated Kernel Subclass Discriminant Analysis (<a href="/project/aksda">AKSDA</a>) method and its combination with SVM classifiers. This is an efficient dimensionality reduction and classification method, for very high-dimensional data.</p>
<p>AKSDA is a new GPU-accelerated, state-of-the-art C++ library (also provided as command-line executable) for supervised dimensionality reduction and classification, using multiple kernels. It greatly reduces the dimensionality of the input data, while at the same time it increases their linear separability. Used in conjunction with linear SVMs, it achieves state-of-the-art classification results, consistently higher than Kernel SVM approaches, at orders-of-magnitude smaller training times.</p>
