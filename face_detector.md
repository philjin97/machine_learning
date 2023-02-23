## Face Detector App
### Step by Step Process
#### 1. Get many faces
#### 2. Make them all black and white
#### 3. Train the algorithm to detect faces 
<br/>

#### pip install python-opencv-headless (Install opencv)
#### print('Code Completed') - error convention? 
#### import cv2 => opencv is a open source library. Download harcascade frontal face data from opencv github. This is a pre-trained machine algorithm trained with many frontal faces. 
#### trained_face_data = cv2.CascadeClassifier('haarcascade_frontalface_default.xml')
#### img = cv2.imread('RDJ.png') => Passing a video or an image to the pre-trained machine algorithm. 
#### cv2.imshow('Clever Programmer Face Detector', img) => Name of the window that pops up in an image form. 
#### cv2.waitKey() => This will keep the previous code and make the window up until a key is pressed to be closed. 
#### grayscaled_img = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY) => changing the color from Red Green Blue to Gray. 

