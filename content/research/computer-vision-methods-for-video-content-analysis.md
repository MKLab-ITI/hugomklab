---
types: research
tags: []
images:
- research/Ambig0_0.jpg
- research/topics.jpg
- research/TrainingProcedureNEW.jpg
- research/TestingProcedure.jpg
- research/sxhma_poster.jpg
- research/nvidia.gif
- research/detrac1.gif
- research/detrac2.gif
- research/graphical_abstract.jpg
layout: research
title: Computer Vision Methods for Video Content Analysis
date: '2016-09-09T14:34:09+03:00'
contact: 
- Kostas Avgerinakis
- Stefanos Vrochidis
- Ioannis (Yiannis) Kompatsiaris
relevant_projects:
- HOMER
- PERICLES
- DemCare
- MEDUSA
- JUMAS
- aceMedia
- beAWARE
- ROBORDER
- CONNEXIONs 
relevant_datasets:
- Dem@Care datasets
---
The widespread proliferation of digital media, and in particular video data, in recent years, has made the automated analysis of its content necessary for retrieval, storage, transmission, security and commercial purposes. Video content is analysed for the detection and recognition of human activities in a variety of setups, ranging from constrained indoors environments to outdoors locations and videos “in the wild” (such as YouTube© content). Applications include health monitoring for ambient assisted living, analysis of online content, effective classification. Video content is also analyzed for the detection of unknown, unusual events and abnormalities using and developing computer vision, machine learning and statistical methods. Applications include security and surveillance applications, in the case of traffic or crowd videos, but also more general videos where abnormal events may occur.

## Human Activity Detection and Recognition

Novel computer vision methods for the detection and recognition of human activities in a wide range of videos, ranging from Ambient Assisted Living (AAL) to sports videos, movie segments and videos "in the wild". Activity detection localizes activities in time, as a precursor to activity recognition. Activity recognition localizes activities in space, by finding their motion boundaries, constructing temporally optimal trajectories, and extracting appearance and motion information on a global and local level and multiple scales. This leads to activity classification or the detection of ambiguous segments/transitions in the video. Discriminative methods with SoA encoding methods like VLAD and Fisher are deployed, achieving very high detection and recognition accuracy. The videos contain color and in some cases also depth information, from which novel descriptors have been created for faster activity recognition. Speeded up activity recognition is also achieved by the use of faster motion estimation methods, based on block matching and MPEG motion vectors, instead of optical flow. Activity recognition for unconstrained videos, with high camera motion, is achieved by the development of novel methods for camera motion compensation, based on multiple homographies.


### Activity detection using Statistical Sequential Boundary Detection (SSBD)

![](/images/research/Dem@Care video trailer_0.gif)

Activity detection automates video understanding, as soon as it spatio-temporally localizes activities throughout unknown videos. In this work we introduced Sequential Statistical Boundary Detection (SSBD), which provides a computationally efficient algorithm that localizes the start and end frames(i.e. boundaries) of predefined activities through an unknown video.

### Rapid action recognition using Spatio-Temporal Activity Cells (STAC) and adaptive background modelling

![](/images/research/Overview.png)

![](/images/research/representationExplanation.png)

![](/images/research/Adaptive_BG_modelling.png)

![](/images/research/activeSTACS_display_blurred.png)

![](/images/research/DemCare2.jpg)

![](/images/research/DemCare3.jpg)

![](/images/research/producedVideoXVID_.gif)

In this work, we introduced spatio-temporal activity cells (STACs) to ) localize humans in video sequences using depth and appearance features for adaptive background modelling. A novel depth feature (HOSNP) that uses Surface normal projections was then combined with the conventional appearance descriptor (HOG) and location information in order to build a computationally efficient and highly accurate action recognition algorithm.

In this work, we introduced spatio-temporal activity cells (STACs) using depth and appearance features for adaptive background modelling that localizes activity presence through a video sequence. A novel depth feature (HOSNP) that uses Surface normal projections was then combined with the conventional appearance descriptor (HOG) and location information in order to build a computationally efficient and highly accurate action recognition algorithm.


### MPEG H.264 video encoding and block matching for fast and efficient action recognition

![](/images/research/block_diagram.png)

In this work, we used MPEG H.264 video encoding to reduce video storage capacity and activity recognition computational cost without losing in classification accuracy. MPEG motion vectors were used to seed a block matching motion estimator, leading almost to real time video processing.

### Motion compensation using motionplanes and multiple homographies

![](/images/research/block_diagram_motionplanes.png)

![](/images/research/Golf0.jpeg)

![](/images/research/Dive29.jpeg)

![](/images/research/handshake2_0.png)

![](/images/research/highfive2_0.png)

![](/images/research/Kick16.jpeg)

![](/images/research/kiss4.png)

Motionplanes is a new way to segment a video sequence by tracking superpixels that follow the same motion pattern over time based on multiple homographies. Motion compensation and action localization can use these features to improve action recognition.

### Mining Discriminative Descriptors for Goal-Based Activity Detection in Smart Environments

![](/files/research/TrainingProcedureNEW.jpg)

![](/files/research/TestingProcedure.jpg)

Human activity detection in relatively constrained environments is continuously gaining more attention in the global research community due to its applications in Smart Environments of Assisted Living. A challenging problem is the automatic detection of activities in continuous video sequences, where subjects freely perform multiple actions within the duration of the video. The temporal detection of the activities (automatic video sequence segmentation) is separated from the recognition (classification) task. Consequently, during the training procedure both a temporal detector and an SVM for activity classification are trained. The temporal detector calculates new, discriminative descriptors from the training data, to be usedd as activity goals during testing in order to assess if the subject is attempting to reach these goals and make real time decisions of activity start/end events. The descriptors produced inside the start/end intervals are collected and used as input to the SVM for the final activity classification.

## Crowd Event Detection for Monitoring, Surveillance, Security

The widespread use of surveillance systems in roads, stations, airports or malls has led to a huge amount of data that needs to be analyzed for safety, retrieval or even commercial reasons. The task of automatically detecting frames with anomalous or interesting events from long duration video sequences has concerned the research community in the last decade. Event, and especially anomaly detection in crowded scenes is considered of huge importance, especially in security applications.

To this end, (near) real-time approaches are being developed for the monitoring and detection of new events in surveillance videos, videos of crowds and temporal textures. Spatiotemporal event and anomaly detection and localization is achieved via the application of methods including statistical sequential change detection, topic models, particle advection principles and swarm theory, as well as relevant computer vision appearance and motion features. Novel descriptors, namely the histograms of oriented swarms, have been introduced and developed for precise spatio-temporal event and anomaly detection in videos of crowds. Statistical methods, including sequential change detection, are applied for the quickest detection of changes and the localization of new events in space and time.

Briefly, the methods that have been developed in MKLab include:

### Topic Model Framework

A topic framework is introduced for unsupervised detection of unusual events, with a focus on traffic and surveillance applications. Each frame is divided into superpixel – based subregions from which spatiotemporal tubes are extracted to be used as documents for further analysis. After feature extraction, a Hierarchical Dirichlet Processes (HDP) mixture model is used to automatically extract representative topics covering the full video dataset. Statistical analysis follows for the segmentiation of video sequences based on the underlying actions in them, while at the same time existing outlier events are detected.

![](/images/research/topics.jpg)

### Swarm Intelligence for detecting Interesting Events

A newly introduced concept based on swarm theory, Histograms of Oriented Swarm (HOS), is applied for successfully capturing scene dynamics. HOS, together with the well known Histograms of Oriented Gradients (HOG), are combined to provide a final descriptor that effectively characterizes each scene. A demo of our method that is based in swarm theory for anomaly detection and localization in crowded scenes can be seen below:

<p><iframe allowfullscreen="" src="https://www.youtube.com/embed/u2v4LaGvVSQ" width="420" height="315" frameborder="0"></iframe></p>

Some sample videos of anomaly detection using our method, applied to the UCSD benchmark dataset (http://www.svcl.ucsd.edu/projects/anomaly/dataset.html) are provided. Rectangles depict the regions of interest (ROIs) in which our algorithm is applied. The blue color contour is the default color of ROIs, while the green contours reveal "anomalies", compared to ground truth. The anomalies detected by our algorithm appear with red colored ROIs.

<p><iframe allowfullscreen="" src="https://www.youtube.com/embed/i_61N5gvU0I?list=PLYmmya8pZ9pUm4VlUEWGQf_v9Xcr8sCZb" width="560" height="315" frameborder="0"></iframe></p>

### Particle Advection for Timely Crowd Event Detection

New approaches were developed for the fast and reliable detection and characterization of abnormal events in crowded scenes, based on particle advection and optical flow estimates. Experiments on benchmark datasets show that changes are reliably detected, while the regions of change are accurately localized. In the figure below a summary of the method is provided.

![](/images/research/sxhma_poster.jpg)

**Sequential Statistical Change Detection**: The application of sequential statistical methods has also been examined for the timely detection of anomalies and new events. Only motion-based features are employed, without resorting to the estimation of optical flow, by modeling the distribution of crowd and temporal texture motion appropriately. As a result, the timely detection of new events is achieved on benchmark datasets.

## Intelligent traffic city management from surveillance systems

Smart city technologies and more specifically assistive transportation and safe driving make up one of the most intriguing domains of computer science and have attracted significant attention during the last decade. Close-Circuit Television (CCTV) systems and other types of visual monitoring infrastructure provide vast amounts of potentially useful data for optimal management of traffic, safety in crowded urban environments, mitigation of traffic issues in adverse weather conditions and numerous other applications of traffic monitoring. Moreover, increasing industry trends towards autonomous driving, vehicles, and transportation in general, is changing the landscape of traffic management. The data from traffic cameras (static, mobile, drone-based and others, depending on the application) will, in the near future, also be used to manage autonomous vehicle navigation, by sending information about events elsewhere in the city, traffic conditions, pedestrian congestion, to optimally guide vehicles. The wealth of information in these videos remains inaccessible without their automated analysis, as the manual extraction of information from them is very time consuming and cumbersome, making automated video analysis methods a necessity.

### Moving Vehicle Detection and Tracking

In this work, we focus on a hybrid object detector, namely DeepHOG, that combines shallow with deep representation schemes and we use it to develop an effective vehicle tracking algorithm in order to track vehicles throughout their full movement on the screen.

More specifically, we used Histograms of Oriented Gradients(HOG) as a local appearance features to represent pedestrians and vehicle objects and encode them into a Fisher vector. This resulted in a powerful mid-level representation vector that maintain the relation difference of each object to the most discriminant ones and provided to a Neural Network in order to train a highly accurate hybrid feature representation.

![](/files/research/method.png)

![](/files/research/nvidia.gif)

![](/files/research/detrac1.gif)

![](/files/research/detrac2.gif)

## Dynamic Texture Recognition and Localization

The term dynamic texture typically refers to moving textures, i.e. visual entities undergoing small, stochastic motions, encountered in real world indoor and outdoor environments. The automatic recognition of such textures has recently attracted attention, as it can provide a significant contribution to many real-world outdoor applications involving: scene analysis containing objects with high varying textures (e.g. water, smoke, trees), security applications for the prevention of a possible terrorist act and surveillance systems, responsible for the avoidance of natural disasters (e.g. fire in the forest or floods).

Even though several methods have been proposed in order to discriminate and classify dynamic textures, they are usually restricted to a global video classification approach, neglecting the necessity of a local aspect, which may prove to be of vital importance in an emergency situation. In order to address this issue, we introduce a novel hybrid framework involving both dynamic texture recognition and localization in outdoors videos captured by surveillance cameras. The LBP-flow descriptor, is investigated and applied to effectively capture textures' motion dynamics while a Principal Component Analysis (PCA)- Fisher scheme is used to address the issues of efficient encoding and handling of high dimensional data. A Neural Network (NN) is fed with the outcome of Fisher encoding, providing a deeper representation of the dynamic texture. Both binary and multi-class classification models are acquired and are used in our novel localization scheme, based on multi-scale superpixel clustering to spatio-temporally detect dynamic textures in videos. The overall recognition and localization framework is depicted in the following figure.

![](/files/research/graphical_abstract.jpg)

Two sample videos on Texture Localization task in water and fire case can be found below.

<p><iframe allowfullscreen="" mozallowfullscreen="" src="https://player.vimeo.com/video/245749802?autoplay=1&amp;loop=1" webkitallowfullscreen="" width="640" height="480" frameborder="0"></iframe></p>

<p><iframe allowfullscreen="" mozallowfullscreen="" src="https://player.vimeo.com/video/246062385?autoplay=1&amp;loop=1" webkitallowfullscreen="" width="640" height="407" frameborder="0"></iframe></p>

---

## Key publications

1. K. Avgerinakis, A. Briassouli, and I. Kompatsiaris, "Activity detection using sequential statistical boundary detection (SSBD)", Computer Vision and Image Understanding (CVIU), March 2016, pp 46-61, vol 144.
 
1. C.F. Crispim-Junior, V. Buso, K. Avgerinakis, G. Meditskos, A. Briassouli, J. Benois-Pineau, I. Kompatsiaris, F. Bremond, “Semantic Event Fusion of Different Visual Modality Concepts for Activity Recognition”, Special Issue on Multimodal Human Pose Recovery and Behavior Analysis, IEEE Transactions on Pattern Analysis and Machine Intelligence (TPAMI), 38(8), pp.1598-1611, 2016, DOI: 10.1109/TPAMI.2016.2537323

1. S. Tachos, K. Avgerinakis, A. Briassouli, I. Kompatsiaris, "Appearance and Depth for Rapid Human Activity Recogntion in Real Applications", British Machine Vision Conference (BMVC), Sep. 2015, pages 38.1-38.12. BMVA Press. DOI: 10.5244/C.29.38.

1. K. Avgerinakis, K. Adam, A. Briassouli, Y. Kompatsiaris, "Moving camera human activity localization and recognition with motionplanes and multiple homographies", IEEE International Conference on Image Processing (ICIP), Quebec city, Canada, Sep. 2015.

1. S. Poularakis, K. Avgerinakis, A. Briassouli, Y. Kompatsiaris, "Computationally efficient recognition of activities of daily living", IEEE International Conference on Image Processing (ICIP),  Quebec city, Canada, Sep. 2015.

1. V. Kaltsa, A. Briassouli, I. Kompatsiaris, L. Hadjileontiadis, M. G. Strintzis, "Swarm Intelligence for Detecting Interesting Events in Crowded Environments", IEEE Trans. on Image Processing, vol 24, issue 7, pp 2153-2166, July 2015. DOI: 10.1109/TIP.2015.2409559

1. K.Avgerinakis, A.Briassouli, I. Kompatsiaris, "Real Time Motion Changes for New Event Detection and Recognition", ACCV 2010 Workshop - 10th International Workshop on Visual Surveillance VS 2010, Queenstown, New Zealand, November 2010, pp 1 - 10.

1. A. Briassouli, I. Kompatsiaris, "Spatiotemporally Localized New Event Detection in Crowds", ARTEMIS ICCV 2011 workshop, Barcelona, November 4-14, 2011, pp 928 - 933.