# Video-Skimming
Assignment 2, Deep Learning (ELL888) @ IIT Delhi

## Problem Statement:

Lots of good quality educational videos are available on platforms like YouTube and NPTEL but students are not able to use them optimally since videos are not indexed properly. This assignment tries to deal with this problem. Have a look at this video: https://goo.gl/VTaz7h
You will notice that, in general, the professor writes on papers, removes that paper that is completely filled and then starts writing again on a new sheet. The aim of this assignment is to extract out those frame of a video which captures the full written content on a sheet of paper.
Suppose the professor writes 7 sheets in one lecture, if we could get the frames capturing those 7 filled sheets, we will have almost all the information of what professor taught in that lecture in just 7 images. One hour video can be summarised using 7 images (Call these 7 frames as ‘key-frames’).
Sometimes, instead of handwritten sheets, other mediums are used to teach in lectures (ppts, notepad etc), but the core problem is still the same, 
Extract minimum frames from videos which cover all the written content.


## Dataset:

There are two folders, ‘frames’ and ‘labels’. ‘frames’ contains frames extracted from videos lectures and ‘lables’ contains csv corresponding to each lecture. 1 denotes ‘key-frames’ and 0 ‘non-key frames’. 

Dataset Available at: https://goo.gl/ckZTTb


## Evaluation Metric:

Metric used for evaluation would be F1-score. Also sometimes multiple consecutive frames will have the same content written on it, so the labels and detections can have a difference of 2 frames but still capture same information. To deal with this, if nth frame was labelled as key, the detection will be considered valid for any frame [n-2, n+2].
