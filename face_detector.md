## Face Detector App
#### Clever Programmer - AI tutorial for beginners YOUTUBE
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
<br/>

#### face_coordinates = trained_face_data.detectMultiScale(grayscaled_img) => detect faces in the image. Returns the coordinates of the rectangle surrounding the face. (x, y, w, h). 
#### (x, y, w, h) = face_coordinates[0] 
#### cv2.rectangle(img, (x,y), (x+w, y+h), (0, 255, 0), 2) => (img, 1st point on the rectangle, 2nd point on the rectangle, color of the rectangle, thickness of the rectangle) 
#### use loops to go through the lists in the list -> for (x,y,w,h) in face_coordinates:
<br/>

## Detecting faces in a video?
#### the only difference is detecting faces through loops.
#### webcam = cv2.VideoCapture(0) => the 0 would mean the default cam
#### while True: 
#### successful_frame_read, frame = webcam.read() => returns a tuple. Returns a true or false value, then the image. 
#### grayscaled_img = cv2.ctvColor(frame, cv2.COLOR_BGR2GRAY)
#### face_coordinates = trained_face_data.detectMultiScale(grayscaled_img)
#### for (x, y, w, h) in face_coordinates:
#### cv2.rectangle(frame, (x,y), (x+w, y+h), (randrange(256), randrange(256), rand))
#### cv2.imshow('Clever Programmer Face Detector', grayscaled_img)
#### cv2.waitKey(1) => if 0, waits until a key is hit. 1, moves with every second. You cannot display something if you don't use waitKey(). 
#### 



