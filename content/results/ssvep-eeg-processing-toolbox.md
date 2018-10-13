---
excerpt: 'Matlab code for proccesing EEG signals'
title: "SSVEP EEG Processing Toolbox"
date: 2018-08-30T13:21:34+03:00
tags:
    - tool
layout: results
types: results
---
This software is released as part of the EU-funded research project MAMEM for supporting experimentation in EEG signals. It follows a modular architecture that allows the fast execution of experiments of different configurations with minimal adjustments of the code. The experimental pipeline consists of the Experimenter class which acts as a wrapper of five more underlying parts;

- The Session object: Used for loading the dataset and segmenting the signal according to the periods that the SSVEP stimuli were presented during the experiment. The signal parts are also annotated with a label according to the stimulus frequency.
- The Preprocessing object: Includes methods for modifying the raw EEG signal.
- The Feature Extraction object: Performs feature extraction algorithms for extracting numerical features from the EEG signals.
- The Feature Selection object: Selects the most important features that were extracted in the previous step.
- The Classification object: Trains a classification model for predicting the label of unknown samples.

For more information [visit github page](https://github.com/MAMEM/eeg-processing-toolbox)