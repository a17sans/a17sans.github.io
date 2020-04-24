# Computer Vision

My aim here is to give a brief overview of the notions that I discovered during my computer vision course at school.

## Geometric transformation, 2D scene reconstruction

A first little exercice was the reconstruction of a landscape based on three images. Based on those images, the basic idea was to use `ORB` for keypoint dectection and matching. 

![alt text](/images/computer_vision/img1.PNG "Initial images")
![alt text](/images/computer_vision/img2.PNG "Keypoint matching")

Those matchings allow us to estimate the geometric transformation between images, to finally reconstruct the landscape. 

![alt text](/images/computer_vision/img3.PNG "Transformation")
![alt text](/images/computer_vision/img4.PNG "Merging")

---

## Semantic segmentation using DL


The idea of segmentation is to detect objetcs in images. The objectives were to use `Keras` library to build convolutional neural nets, and see the influence of its construction. 

![alt text](/images/computer_vision/img5.PNG "Deep learning method")

We saw dice scores increase with the following constructions : 
- 7 convolutional layers in a Fully Convolutional Network (FCN)
- 5 patterns of 2 convolutional layers seperated by MaxPooling 
- same construction but using concatenation
- use VGG16 pre-trained on the ImageNet dataset, with MaxPooling

![alt text](/images/computer_vision/img6.PNG "Results")


---

## Optical flow

We understood in this lab the basic ideas of optical flow estimation, by implementing the famous **Horn and Schunk** method, and comparing it to **Lucas Kanade**. We tried to get the distribution of velocities by using spatial and temporal gradients.

![alt text](/images/computer_vision/img7.PNG "Optical flow")

We also understood issues in long term motion estimation, by implementing two functions for mask propagation with direct and sequential integration. 

---

## Stereovision

We understood here geometrical properties, implied by calibration (we used **OpenCV**), and the parameters resulting from it.
We did in this lab pose estimation, by keypoint extraction and matching, finding the fundamental matrix, plottting some epipolar lines, and then find pose estimation.


