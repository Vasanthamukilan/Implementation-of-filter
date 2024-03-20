# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.
### Step2
Convert the image from BGR to RGB.
### Step3
Apply the required filters for the image separately.
### Step4
Plot the original and filtered image by using matplotlib.pyplot.
### Step5
End the program.

## Program:
### Developed By:Vasanthamukilan M
### Register Number:212222230167
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('cheetah.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

kernel = np.ones((11,11), np. float32)/121
image3 = cv2.filter2D(image2, -1, kernel)

plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('Orignal')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv) Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```
### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```
## OUTPUT:
### 1. Smoothing Filters
i) Using Averaging Filter
</br>![download1](https://github.com/Vasanthamukilan/Implementation-of-filter/assets/119559694/442e86c2-769d-4068-b947-483c7a657d4d)</br>

ii) Using Weighted Averaging Filter
</br>![download2](https://github.com/Vasanthamukilan/Implementation-of-filter/assets/119559694/361a8e3d-60d8-4ffd-a087-2238de64ff9b)</br>

iii) Using Gaussian Filter
</br>![download3](https://github.com/Vasanthamukilan/Implementation-of-filter/assets/119559694/244ce7b7-cca1-4638-9f70-4c787744610d)</br>

iv) Using Median Filter
</br>![download4](https://github.com/Vasanthamukilan/Implementation-of-filter/assets/119559694/0574ec6b-98db-4302-9fd2-e2a434812616)</br>

### 2. Sharpening Filters
i) Using Laplacian Kernal
</br> ![download5](https://github.com/Vasanthamukilan/Implementation-of-filter/assets/119559694/10ed4f07-0435-4af3-be15-351dcea441d3)</br>

ii) Using Laplacian Operator
</br>![download6](https://github.com/Vasanthamukilan/Implementation-of-filter/assets/119559694/355fcd64-5724-4816-beaf-1d7dcec10ffe)</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
