* Object Representation

* Single target tracking

* Multi-target tracking


A good detector is the key. 


### Definitions

Online Tracking and Offline Tracking. 

Online Tracking: only the previous frame and current frame are available. 

Offline Tracking (batch tracking): all frames are available 

Data Association: The association of detection between frames. 
* Two frame methods: simple and suitable for online tracking 
* Multiple frame methods: consider the whole video

Affinity = Similarity

Simple Association: Overlapping between IoU of previous frame and current frame. For each track, select the detection with the hightest IoU. If IoU is larger than threshold, add this IoU to the track and remove it from the list of unassociated detections. If the best overlap is still lower than the threshold then finish the track. If the track is too short or had no higher confidence directions, consider the track false positives and then remove it from the final list of tracks. 


Simple Online and Realtime Tracking (SOR)
* CNN-based object detector
* Kalman Filter for prediction of object position in current frame based on positions in previous frames.
* Hungarian alogirthm for matching object detections in curerent frames with predicted positions. 
* IoU of detected and predicted bounding boxes for matching detection track.

Reduces ID switches (ID sw), False negatives, Mostly Lost (ML) and increases Mostly Tracked (MT).

Points of observed scene are moving relative to the camera 
Vector fields of 2D projections of scene point motion vectors is called motion field

Capture the motion field using Optical Flow. Optical Flow is the vector field 

Dataset: 
DETRACK-dataset


## Videos
[1. Introduction to Video Analysis](https://www.coursera.org/lecture/deep-learning-in-computer-vision/introduction-to-video-analysis-alApg)

[2. Examples of multiple object tracking methods](https://www.coursera.org/lecture/deep-learning-in-computer-vision/examples-of-multiple-object-tracking-methods-VJZUW)

[3. Optical Flow](https://www.coursera.org/lecture/deep-learning-in-computer-vision/optical-flow-2wMqQ)

## Articles:

[Simple Tracking with OpenCV](https://www.pyimagesearch.com/2018/07/23/simple-object-tracking-with-opencv/)

## Lecture Slides

CS231-Stanford University:
http://vision.stanford.edu/teaching/cs231b_spring1415/slides/lectureTracking.pdf

## References:

#### Tracking	by	matching	
– Isard,	Michael,	and	Andrew	Blake.	"CondensaEon—	condiEonal	density	propagaEon	
for	visual	tracking."	InternaEonal	journal	of	computer	vision	29.1	(1998):	5-28.

– S.	Oron,	A.	Bar-Hillel,	D.	Levi,	and	S.	Avidan.	Locally	Orderless	Tracking.	In	CVPR,	2012

#### Tracking	by	matching	with	an	extended	appearance	model	
– D.	Ross,	J.	Lim,	R.-S.	Lin,	and	M.-H.	Yang.	Incremental	Learning	for	Robust	Visual	
Tracking.	IJCV,	77(1):125–141,	2008.	

#### Tracking	with	sparsity	constraint	
– W.	Zhong,	H.	Lu,	and	M.-H.	Yang.	Robust	Object	Tracking	via	Sparsity-based	
CollaboraEve	Model.	In	CVPR,	2012.	

– Kwon,	Junseok,	and	Kyoung	Mu	Lee.	"Visual	tracking	decomposiEon."Computer
Vision	and	Pauern	RecogniEon	(CVPR),	2010	IEEE	Conference	on.	IEEE,	2010.	\

– Li,	Hanxi,	Chunhua Shen,	and	Qinfeng	Shi.	"Real-Eme	visual	tracking	using	
compressive	sensing."	Computer	Vision	and	Pauern	RecogniEon	(CVPR),	2011	IEEE	
Conference	on.	IEEE,	2011.	

#### Tracking	by	detecEons	(ML	approach,	using	a	discriminaEve	classificaEon)	
– Babenko,	Boris,	Ming-Hsuan	Yang,	and	Serge	Belongie.	"Visual	tracking	with	online	
mulEple	instance	learning."	Computer	Vision	and	Pauern	RecogniEon,	2009.	CVPR	
2009.	IEEE	Conference	on.	IEEE,	2009.	

– Z.	Kalal,	K.	Mikolajczyk,	and	J.	Matas,	“Tracking-Learning-DetecEon,”	Pauern	Analysis	
and	Machine	Intelligence	2011.	

– S.	Hare,	A.	Saffari,	and	P.	H.	S.	Torr.	Struck:	Structured	Output	Tracking	with	Kernels.	
In	ICCV,	2011.	

– F.	Henriques,	R.	Caseiro,	P.	MarEns,	and	J.	BaEsta.	ExploiEng	the	Circulant	Structure	of	
Tracking-by-DetecEon	with	Kernels.	In	ECCV,	2012	

– Nebehay,	Georg,	and	Roman	Pflugfelder.	"Consensus-based	matching	and	tracking	of	
keypoints	for	object	tracking."	ApplicaEons	of	Computer	Vision	(WACV),	2014	IEEE	
Winter	Conference	on.	IEEE,	2014.	
