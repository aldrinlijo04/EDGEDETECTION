# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import the required packages for further process.

### Step 2:
Read the image and convert the bgr image to gray scale image.

### Step 3:
Use any filters for smoothing the image to reduse the noise.

### Step 4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step 5:
Display the filtered image using plot and imshow.

## Program:
```
DEVELOPED BY : ALDRIN LIJO J E
REG NO : 212222240007
```
## Import the packages
```
import cv2
import matplotlib.pyplot as plt
```
# Load the image, Convert to grayscale and remove noise
```
img=cv2.imread("Cute-Cat.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
# SOBEL EDGE DETECTOR:
# SOBEL X AXIS :
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
# SOBEL Y AXIS :
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
# SOBEL XY AXIS :
```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
# LAPLACIAN EDGE DETECTOR
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
# CANNY EDGE DETECTOR
```
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
# SOBEL X AXIS :
![download](https://github.com/aldrinlijo04/EDGEDETECTION/assets/118544279/9e6455c6-6719-47e8-b728-27441f832b8a)

# SOBEL Y AXIS :
![download](https://github.com/aldrinlijo04/EDGEDETECTION/assets/118544279/04908c42-8057-4b78-a5e6-9882c07181e1)

# SOBEL XY AXIS :
![download](https://github.com/aldrinlijo04/EDGEDETECTION/assets/118544279/fb22835d-493e-480e-802c-0bab3ac8dec2)

### LAPLACIAN EDGE DETECTOR
![download](https://github.com/aldrinlijo04/EDGEDETECTION/assets/118544279/c101cfe6-d541-4f56-8e63-ae3e592335f4)

### CANNY EDGE DETECTOR
![download](https://github.com/aldrinlijo04/EDGEDETECTION/assets/118544279/d8a1de39-017b-4609-8d6c-82e7a6aa0a4e)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
