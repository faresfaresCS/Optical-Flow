# Optical-Flow
Optical Flow in OpenCV (Python)

# What is Optical Flow?
Optical flow is a task of per-pixel motion estimation between two consecutive frames in one video. Basically, the Optical Flow task implies the calculation of the shift vector for pixel as an object displacement difference between two neighboring images. The main idea of Optical Flow is to estimate the object’s displacement vector caused by it’s motion or camera movements.

# Optical Flow applications
Optical Flow can be used in many areas where the object’s motion information is crucial. Optical Flow is commonly found in video editors for compression, stabilization, slow-motion, etc. Also, Optical Flow finds its application in Action Recognition tasks and real-time tracking systems.

# Lucas-Kanade implementation with OpenCV
OpenCV has the implementation of Pyramid Lucas & Kanade with Shi-Tomasi algorithm improvement (https://docs.opencv.org/2.4/modules/video/doc/motion_analysis_and_object_tracking.html#calcopticalflowpyrlk) to calculate the Optical Flow. Let’s take a look at the OpenCV algorithm based on official documentation.

In short, main.py script takes two consecutive frames and finds the corners on the first one with cv2.goodFeaturesToTrack function. After that, we compute the Optical Flow with the Lucas-Kanade algorithm using the information about the corner location. This is a cycled process which does the same for each pair of consecutive images.

To run the Lucas-Kanade demo you can use the following command:
python3 main.py --algorithm lucaskanade --video_path videos/PATH_TO_VIDEO/*.mp4

