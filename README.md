# Head-Pose-Estimation
This is a Supervised Machine Learning Models, extract features using mediapipe the use Regression models by sklearn with visualization, from '2D' landmarks not 3D landmarks..
To do so with the classical way they have to fit the 2D points with a 3D face model which is considered as a fitting technique. 
At the end, it is not a deterministic solution and has its problems.
Here comes the ML to replace the 3D fitting assumption, the camera parameters and the  projection equations.

### Source Video
![Game Process](https://github.com/omaraz/Head-Pose-Estimation/blob/main/Ms_Pre.gif)

### After predicting Pitch, Yaw and Roll Axes Video
![Game Processs](https://github.com/omaraz/Head-Pose-Estimation/blob/main/Ms_post.gif)
### Project Description
- Our goal in this project to predict head pose estimation with 3 axes (Pitch, Yaw, Roll) face geometry using [AFLW2000 Dataset](http://cvlab.cse.msu.edu/lfw-and-aflw2000-datasets.html) by using 3 Regression models.
- This Dataset includes 2000 images contain faces so we use *mediapipe* library to extact face points as features(468 points (x,y)) so we have 468 * 2 so final features count  = 936.
- Then extract labels from matlab file that related to each image we have three labels as output the 3 axes (Pitch, Yaw, Roll) values.
- We will use MediaPipe library in both training and testing phases:
  - In Training: first we dtect the face of each image then using the same library to generate the landmark points of the face after this phase the training data (features) will contain 1853 samples with 936 columns (468 for X and 468 for Y), for labels we will extract the 3 angels from the mat file. 
  - In Testing: we will use the MediaPipe Library to generate the landmarks as we did in the training phase and using the trained models to predict the 3 labels and using them to draw the axis.  
### So, Let's Start 😃 
### The Office fans will enjoy some of this project 😎
