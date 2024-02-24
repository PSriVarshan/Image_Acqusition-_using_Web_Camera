# Image Acqusition using Web Camera
## Aim
 
#### To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
##### i) Write the frame as JPG 
##### ii) Display the video 
##### iii) Display the video by resizing the window
##### iv) Rotate and display the video

## Software 

### Anaconda - Python 3.7

## Algorithm

### Step 1:

#### Use cv2.VideoCapture(0) to access web camera

### Step 2:

#### Use cv2.imread to read the video or image

### Step 3:

#### Use cv2.imwrite to save the image

### Step 4:

#### Use cv2.imshow to show the video

### Step 5:

End the program and close the output video window by pressing 'q'.

## Program:

### Developed By: Sri Varshan P
### Register No: 212222240104

#### i) Write the frame as JPG file
```py
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("SriVarshan.jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```
#### ii) Display the video
```py
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('Shangai',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()

```
#### iii) Display the video by resizing the window
```py
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222240104-PsvVarshan,image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
#### iv) Rotate and display the video

```py
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222240104_PsvVarshan',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image
</br>

![image](https://github.com/PSriVarshan/Image_Acqusition-_using_Web_Camera/assets/114944059/a28440d8-9167-4fc2-9355-92fa8fb3f512)

</br>


### ii) Display the video
</br>

![image](https://github.com/PSriVarshan/Image_Acqusition-_using_Web_Camera/assets/114944059/1156044e-5939-4941-8889-bfd4d48d6015)

</br>


### iii) Display the video by resizing the window
</br>

![image](https://github.com/PSriVarshan/Image_Acqusition-_using_Web_Camera/assets/114944059/e21bb44c-7aba-4cc1-b8fe-f3ae63f36d82)


</br>



### iv) Rotate and display the video
</br>

![image](https://github.com/PSriVarshan/Image_Acqusition-_using_Web_Camera/assets/114944059/7baf375c-560d-4804-8fa7-1a80617893b7)

</br>





## Result:
### Thus the image is accessed from webcamera and displayed using openCV.
