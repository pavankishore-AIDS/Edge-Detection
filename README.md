# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>
Import the necessary modules.

### Step2:
<br>
Load the image to operate on.

### Step3:
<br>
Convert the image to grayscale image.

### Step4:
<br>
Use Sobel operator along x,y and xy directions.

### Step5:
<br>
Operate the image using Laplacian operator.

### Step6:
<br>
Operate the image using Canny Edge operator.

### Step7:
<br>
Show all the operated images output.

## Program:

``` Python
# Import the packages
import cv2
import numpy as np
import matplotlib.pyplot as plt


# Load the image, Convert to grayscale and remove noise
image1=cv2.imread ('baki.jpeg') 
gray_image = cv2.cvtColor(image1,cv2.COLOR_BGR2GRAY)

cv2.imshow('Gray',gray_image)


# SOBEL EDGE DETECTOR
img = cv2.GaussianBlur(gray_image,(3,3),0)
sobelx = cv2.Sobel(gray_image,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(gray_image,cv2.CV_64F,0,1,ksize=5)
sobelxy =cv2.Sobel(gray_image,cv2.CV_64F,1,1,ksize=5)
cv2.imshow('Sobel X',sobelx)
cv2.imshow('Sobel Y',sobely)
cv2.imshow('Sobel XY',sobelxy)


# LAPLACIAN EDGE DETECTOR
laplacian=cv2.Laplacian(img,cv2.CV_64F)
cv2.imshow('Laplacian',laplacian)


# CANNY EDGE DETECTOR
canny_edges = cv2.Canny(gray_image, 120, 150)
cv2.imshow('Canny Edges',canny_edges)

cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:
### GRAYSCALE IMAGE
![Screenshot (15)](https://user-images.githubusercontent.com/94154941/234509017-dd70d670-968e-4574-a25c-cc9a687b02d2.png)


### SOBEL EDGE DETECTOR

![Screenshot (14)](https://user-images.githubusercontent.com/94154941/234509086-9c41bd3f-8122-4868-b078-a2bf8d2b47bd.png)

![Screenshot (12)](https://user-images.githubusercontent.com/94154941/234509174-2e93a057-b7cb-4f85-9743-5312c4ce2193.png)

![Screenshot (13)](https://user-images.githubusercontent.com/94154941/234509141-c4d423c6-cb66-43ce-ae53-5220e0e1368d.png)



### LAPLACIAN EDGE DETECTOR
![Screenshot (11)](https://user-images.githubusercontent.com/94154941/234509226-00debe66-37df-4c47-895b-44df0c23fddd.png)


### CANNY EDGE DETECTOR
![Screenshot (10)](https://user-images.githubusercontent.com/94154941/234509242-480a66bf-9329-46da-81d4-161317f5e9eb.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
