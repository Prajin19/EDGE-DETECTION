# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## Program:
```
Developed by : Prajin S
Register Number : 212223230151
```
### Loading the Images :
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('cow.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.subplot(1, 1, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR
```python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5) 
sobel_combined = cv2.magnitude(sobel_x, sobel_y) 
plt.subplot(1,1,1)
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```python
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.subplot(1,1,1)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```python
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.subplot(1,1,1)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
## Output:
### Original Image
![image](https://github.com/user-attachments/assets/86d87aaa-861b-4ae2-996b-74e5f515cdac)

### SOBEL EDGE DETECTOR
![image](https://github.com/user-attachments/assets/3f5f8685-1309-442c-9810-d93503bb9aaf)


### LAPLACIAN EDGE DETECTOR
![image](https://github.com/user-attachments/assets/0b19f6d7-2225-4882-88bf-3993d85cf593)


### CANNY EDGE DETECTOR
![image](https://github.com/user-attachments/assets/760eb6ec-9c6a-4d5a-91d1-94f10bf4ff5a)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
