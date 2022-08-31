Motion Detection and tracking using python and OpenCV




https://user-images.githubusercontent.com/20885138/187669707-2f027ad8-3adf-446f-8e58-679ed3b193d3.mp4
:

Object Detection is a well-known computer technology combined with computer vison and image processing that focuses on detecting objects or its instances of certain class such as human flowers and animals in digital images and videos.
There are various applications of object detection that have been well researched including face detection and character recognitions, and vehicle calculator. 

Problem description 


There are practical requirements of miniaturization and high efficiency of motion detection and tracking embedded system. Video Motion Detection is a way of defining activity in a scene by analyzing the difference occur in a series of images, this is usually done by pixel mating or frame referencing, any changes between frames is called as ‘detection’.

Object detection could be used for various purpose including retrieval and surveillance etc.
In order to further maintain peace and provide security to people now a days Closed-circuit television (CCTV) surveillance system is being utilized, this is designed and implement on low cost security camera with nigh vision capability using Raspberry Pi (RPI) and (OpenCV).
It is designed to facilitate inside warehouse facilities.
It has human detection and smoke detection capabilities that can provide precaution to potential crimes and fire.



State of the art references

In computer vision and machine learning, tracking is a very broad term that encompasses conceptually similar but technically different ideas. For example, all the following different but related ideas are generally studied under Object Tracking.


Single object trackers: In this class of trackers, the first frame is marked using a rectangle to indicate the location of the object we want to track. The object is then tracked in subsequent frames using the tracking algorithm. 
In most real-life applications, these trackers are used in conjunction with an object detector. 

Multiple object track finding algorithms: In cases when we have a fast object detector, it makes sense to detect multiple objects in each frame and then run a track finding algorithm that identifies which rectangle in one frame corresponds to a rectangle in the next frame.

Background subtraction: is critical in many computer vision applications. We use it to count the number of cars passing through a toll booth. We use it to count the number of people walking in and out of a store and we use it for motion detection. [2]

The two primary methods are forms of Gaussian Mixture Model-based foreground and background segmentation: 
An improved adaptive background mixture model for real-time tracking with shadow detection by KaewTraKulPong et al., available through the cv2.BackgroundSubtractorMOG function. 

Improved adaptive Gaussian mixture model for background subtraction by Zivkovic, and Efficient Adaptive Density Estimation per Image Pixel for the Task of Background Subtraction, also by Zivkovic, available through the cv2.BackgroundSubtractorMOG2 function.

Theory of solution 

The goal of this project is to determine the global motion gradient of a foreground object using live cam or recorded videos, the usage of a camera (Computer Vision), coding in python, Deep learning, Algorithms, Data models are being used to find the better solution.
As the hardware recourses were not available so the experimentation was conducted on the laptop Camera (Live Cam), surveillance of vehicle and the data provided by Beril on GitHub. 

Following are the useful Implementations of the application.

Monitoring Applications Surveillance 
Security Cameras 
Traffic Monitoring Traffic Monitoring 
People Counting 


Control Applications
Object Avoidance Object Avoidance 
Automatic Guidance 
Head Tracking for Video Head Tracking for Video Conferencing

Detection of motion is being discussed under the following application.

Moving objects can be detected by applying Background Subtraction Algorithms
Simplest method (frame differencing) 
Subtract consecutive frames 
Ideally this will leave only moving objects 

Following conditions effect the background subtraction 

Moving background (e.g. swaying of trees) 
Temporarily stationary objects 
Object shadows Object shadows 
Illumination variation

Working:

All we need is to detect moving objects in a video stream(source being camera here). There are multiple images or frames which are displayed very quickly. So using OpenCV, we will capture the frames and will loop through each frame so that it appears like a video. To detect the moving objects, we will store the first image as the base frame and then with each further frames we will keep on subtracting the frames, so that if at any point of time there is a difference b/w the two frames it means there is a new object in our frame, then we will detect that new object in our frame and will highlight in into the windows by drawing a rectangle around it. [1]
To increase the efficiency, we would convert each frame to gray scale and then Gaussian blur image. Also a threshold is defined to remove minor deviations in the frame, e.g., shadows, flies, etc. as we are really not interested in detecting those as our desired objects.

The following Screenshots of working application shows the input frame, difference between two frame showing moving object and binary image of difference image.

Limitations 
The proposed method also detects the motion due to the movement in air. As the air moves, the camera not remains in the position of static so when there is no movement of object then also it results motion and shows holes in the binary output image.[3]


Motivation to choose this theory 

The following methodology provide a complex method of learning outcomes of computer vision on live detection of object including flower, human face as well, now a days due to COVID-19 many applications are being designed for social distance, through live detection body temperature measurement, Face-mask detection are also being in discussion. Following are the useful Implementations of the object detection.

Monitoring Applications Surveillance 
Security Cameras 
Traffic Monitoring Traffic Monitoring 
People Counting 


Control Applications
Object Avoidance Object Avoidance 
Automatic Guidance 
Head Tracking for Video Head Tracking for Video Conferencing
Hence it was getting really attractive topic for discussion now a days so we decided to work on it secondly it was a great experience to work on latest technologies, we will be willing to work more in future and embedded on hardware devices as well.

Result:

In the present research, moving object is detected by the method of motion detection, which composes of frame difference method and morphological operations. The obvious keystone of the work is studying the principle of frame difference method and to resolve the various problems. The experiment shows that the method has good performance and efficiency.

we learned how to use the frame differencing technique to perform moving object detection in videos. We also covered several concepts and topics around object detection and image processing. Then we went on to build our own moving object detection system using OpenCV.


References: 

K.Kavitha, A.Tejaswini, Background Detection and Subtraction for Image Sequences in Video, International Journal of Computer Science and Information Technologies, vol.3, Issue 5, pp. 5223-5226, 2012

An improved adaptive background mixture model for real-time tracking with shadow detection by KaewTraKulPong et al., available through the cv2.BackgroundSubtractorMOG function. 

Improved adaptive Gaussian mixture model for background subtraction by Zivkovic, and Efficient Adaptive Density Estimation per Image Pixel for the Task of Background Subtraction, also by Zivkovic, available through the cv2.BackgroundSubtractorMOG2 function.

ZhengjieWang, YuanZhao, JifenZhang, YinjingGuo, Research on Motion Detection of Video Surveillance System, 3 rd International Congress on Image and SignalProcessing, vol.1, pp. 193-197, October 2010

