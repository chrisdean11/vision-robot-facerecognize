# vision-robot-facerecognize
ROS Node that uses OpenCV 2.4 to perform face detection and recognition. Listens for published images from a Kinect or webcam, performs image analysis, and tells the robot where to turn its head to follow the individual.

This ROS node is a robotics and computer vision project that's part of a larger system developed by students at Portland State University. MCECSBot "Jeeves" is a tour guide humanoid robot at the Electrical and Computer Engineering department.

This node only works as part of that system, unless a user were to change the source code to subscribe/publish to their own custom topics. Please see the PDF writeup I did for a detailed analysis of the various available recognition algorithms and the overall functionality of this node if you intend to customize it.

My program uses a Haar Cascade Classifier that comes standard with OpenCV to perform face detection. When a face is detected in the video stream, it's cropped out and compared to my recogntion model.

The LBPH model provided was trained by me to recognize a few different students and professors at PSU.

Finally, the location of the detected face is published to its own topic. The robot's head control node receives this location and tracks the individual with its head for a cool/creepy effect.

Enjoy!
