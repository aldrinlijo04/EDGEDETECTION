# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.
<br>


### Step2:
Read the image and convert the bgr image to gray scale image.
<br>

### Step3:
Use any filters for smoothing the image to reduse the noise.
<br>

### Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.
<br>

### Step5:
Display the filtered image using plot and imshow.
<br>

 
## Program:
```
DEVELOPED BY: ALDRIN LIJO J E
REG NO : 212222240007
```

 Python
```
# Import the packages
import cv2
import matplotlib.pyplot as plt
```

# Load the image, Convert to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("dipt.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

# SOBEL EDGE DETECTOR
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
###  SOBEL X AXIS :

![download](https://github.com/aldrinlijo04/EDGEDETECTION/assets/118544279/31fa703f-485a-4d65-80b0-645a730451d2)



###  SOBEL Y AXIS :


![download](https://github.com/aldrinlijo04/EDGEDETECTION/assets/118544279/9b1d1e72-98f2-4d38-9099-20ad24e0b1ee)


###  SOBEL XY AXIS :


![download](https://github.com/aldrinlijo04/EDGEDETECTION/assets/118544279/b73c2bea-5c5d-4487-8cf2-6d3fa8b4eb0d)

<br>


### LAPLACIAN EDGE DETECTOR

![download](https://github.com/aldrinlijo04/EDGEDETECTION/assets/118544279/00aec6e1-9125-4d9e-87d5-bd812e0db608)


<br>


### CANNY EDGE DETECTOR

![download](https://github.com/aldrinlijo04/EDGEDETECTION/assets/118544279/a4f9ff37-8393-4c14-9648-5f10cb345933)


<br>

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
