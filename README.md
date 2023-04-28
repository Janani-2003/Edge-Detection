# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>Import the required packages for further process.


### Step2:
<br>Read the image and convert the bgr image to gray scale image.

### Step3:
<br>Use any filters for smoothing the image to reduse the noise.

### Step4:
<br>Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step5:
<br>Display the filtered image using plot and imshow.

 
## Program:
### Developed by : JANANI R
### Register no : 212221230039
``` Python
# Import the packages
import numpy as np
import cv2
import matplotlib.pyplot as plt


# Load the image, Convert to grayscale and remove noise
img=cv2.imread ('pop.jpg')
img1=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
plt.title('Original_image')
plt.imshow(img1)

gray_img = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
plt.title('GRAY_IMAGE')
plt.imshow(gray_img,cmap = 'gray')

# SOBEL EDGE DETECTOR
img = cv2.GaussianBlur(gray_img,(3,3),0)
sobelx = cv2.Sobel(gray_img,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(gray_img,cv2.CV_64F,0,1,ksize=5)
sobelxy =cv2.Sobel(gray_img,cv2.CV_64F,1,1,ksize=5)

plt.figure(1)
plt.subplot(1,1,1)
plt.imshow(gray_img,cmap = 'gray')
plt.title('Original'), plt.xticks([]), plt.yticks([])

# SOBELx : 

plt.subplot(1,1,1)
plt.imshow(sobelx,cmap='gray')
plt.title('sobelx')
plt.xticks([]), plt.yticks([])

# SOBELy : 

plt.subplot(1,1,1)
plt.imshow(sobely,cmap='gray')
plt.title('sobely')
plt.xticks([]), plt.yticks([])

# SOBELxy : 

plt.subplot(1,1,1)
plt.imshow(sobelxy,cmap='gray')
plt.title('sobelxy')
plt.xticks([]), plt.yticks([])
plt.show()

# LAPLACIAN EDGE DETECTOR
laplacian = cv2.Laplacian(gray_img,cv2.CV_64F)
plt.imshow(laplacian,cmap='gray')
plt.title('laplacian')
plt.show()


# CANNY EDGE DETECTOR
canny_edges = cv2.Canny(gray_img, 120, 150)
plt.imshow(canny_edges,cmap='gray')
plt.title('canny_edges')
plt.show()



```
## Output:
### ORIGINAL IMAGE
![pop1](https://user-images.githubusercontent.com/94288340/235216430-0e5e9740-c1b2-40fb-9de7-89aea76bd1c7.png)

### SOBEL EDGE DETECTOR
### Sobel x
<br>![sobelx](https://user-images.githubusercontent.com/94288340/235216100-de8d402a-e0e0-41ef-aaec-f1a14250eb03.png)
<br>
### Sobel y
<br>![sobely](https://user-images.githubusercontent.com/94288340/235216162-04daa864-3de1-4f11-a03a-8c16169c8b7b.png)
<br>
### Sobel xy
<br>![sobelxy](https://user-images.githubusercontent.com/94288340/235216207-da431f6a-2426-47c7-acc3-bb31b391871a.png)
<br>
### LAPLACIAN EDGE DETECTOR
<br>![laplacian](https://user-images.githubusercontent.com/94288340/235216295-3904c6b9-fae7-4ec3-a295-c666cf2613b9.png)
<br>
<br>
<br>
### CANNY EDGE DETECTOR
<br>![canny](https://user-images.githubusercontent.com/94288340/235216335-b4052856-37d0-4be1-b015-e970adc7bdd8.png)
<br>
<br>
<br>

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
