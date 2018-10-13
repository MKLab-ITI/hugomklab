---
excerpt: 'Support Vector Machine with Gaussian Sample Uncertainty (SVM-GSU) is a maximum margin classifier that deals with uncertainty in data input'
types: results
tags:
- tool
images: []
layout: results
title: SVM-GSU
date: '2017-12-06T13:26:19+02:00'
---
![Support Vector Machine with Gaussian Sample Uncertainty](https://mklab.iti.gr/files/SVM-GSU.png)


**Motivation of the linear SVM-GSU**:*The proposed classifier takes input data uncertainty (modeled as multivariate anisotropic Gaussians) into consideration, leading to a (probably drastically) different decision border (solid line), compared to the standard linear SVM (dashed line) that would consider only the means of the Gaussians, ignoring the various uncertainties.*

Support Vector Machine with Gaussian Sample Uncertainty (SVM-GSU) is a maximum margin classifier that deals with uncertainty in data input. More specifically, we reformulate the SVM framework such that each training example can be modeled by a multi-dimensional Gaussian distribution described by its mean vector and its covariance matrix - the latter modeling the uncertainty. We address the classification problem and define a cost function that is the expected value of the classical SVM cost when data samples are drawn from the multi-dimensional Gaussian distributions that form the set of the training examples. Our formulation approximates the classical SVM formulation when the training examples are isotropic Gaussians with variance tending to zero. We arrive at a convex optimization problem, which we solve efficiently in the primal form using a stochastic gradient descent approach. The resulting classifier, which we name SVM with Gaussian Sample Uncertainty (SVM-GSU), is tested on synthetic data and five publicly available and popular datasets; namely, the MNIST, WDBC, DEAP, TV News Channel Commercial Detection, and TRECVID MED datasets. Experimental results verify the effectiveness of the proposed method.

A C++ framework for the Support Vector Machine with Gaussian Sample Uncertainty (SVM-GSU), whose

- linear variant **(LSVM-GSU)** was first proposed in **[1]**, and
- its kernel version, i.e., Kernel SVM with Isotropic Gaussian Sample Uncertainty **(KSVM-iGSU)**, was first proposed in **[2]**

The framework is available at https://github.com/chi0tzp/svm-gsu

If you want to use one of the above classifiers, please consider citing the appropriate paper(s):  
[1] C. Tzelepis, V. Mezaris, I. Patras, *"Linear Maximum Margin Classifier for Learning from Uncertain Data"*, IEEE Transactions on Pattern Analysis and Machine Intelligence, accepted for publication. [DOI:10.1109/TPAMI.2017.2772235](https://ieeexplore.ieee.org/document/8103808/). An alternate preprint version is available [here](https://www.researchgate.net/publication/275054882_Linear_Maximum_Margin_Classifier_for_Learning_from_Uncertain_Data).

[2] C. Tzelepis, V. Mezaris, I. Patras, *"Video Event Detection using Kernel Support Vector Machine with Isotropic Gaussian Sample Uncertainty (KSVM-iGSU)"*, Proc. 22nd Int. Conf. on MultiMedia Modeling (MMM'16), Miami, FL, USA, Springer LNCS vol. 9516, pp. 3-15, Jan. 2016. [DOI:10.1007/978-3-319-27671-7_1](https://doi.org/10.1007/978-3-319-27671-7_1). An alternate preprint version is available [here](https://www.researchgate.net/publication/302103593_Video_Event_Detection_using_Kernel_Support_Vector_Machine_with_Isotropic_Gaussian_Sample_Uncertainty_KSVM-iGSU).
