# IMPLEMENTATION-OF-FILTERSS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
 Import Necessary Libraries

### Step2
Load the image you want to process using the chosen library.

### Step3
Define the filter kernel for smoothing or sharpening as a 2D matrix.

### Step4
Apply the filter to the image using cv2.filter2D

### Step5
Display or save the processed image using cv2.imshow

## Program:
### Developed By:  Lubindher S
### Register Number: 212222240056
</br>

### 1. Smoothing Filters:
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("tree.png")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
```
i) Using Averaging Filter
```Python
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")




```
ii) Using Weighted Averaging Filter
```Python

kernel2=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel2)
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
gaussian_blur=cv2.GaussianBlur(src=image2,ksize=(33,33),sigmaX=0,sigmaY=0)
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
median=cv2.medianBlur(src=image2,ksize=11)
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
kernel3=np.array([[0,-1,-1],[2,-4,1],[2,1,0]])
image3=cv2.filter2D(image2,-1,kernel3)
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
new_image=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(new_image)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()





```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter:

![image](https://github.com/Jayakrishnan22003251/IMPLEMENTATION-OF-FILTERSS/assets/120232371/984a5bc8-982b-4466-990a-9f30329cd24a)


ii) Using Weighted Averaging Filter:

![image](https://github.com/Jayakrishnan22003251/IMPLEMENTATION-OF-FILTERSS/assets/120232371/6f278e0a-1ece-4865-a067-0688be544341)


iii) Using Gaussian Filter:

![image](https://github.com/Jayakrishnan22003251/IMPLEMENTATION-OF-FILTERSS/assets/120232371/6829c20d-31ec-4fdf-8f01-8f1d364be383)




iv) Using Median Filter:

![image](https://github.com/Jayakrishnan22003251/IMPLEMENTATION-OF-FILTERSS/assets/120232371/1b40067a-cd85-46ed-a129-0724f3a70f9b)




### 2. Sharpening Filters


i) Using Laplacian Kernal:

![image](https://github.com/Jayakrishnan22003251/IMPLEMENTATION-OF-FILTERSS/assets/120232371/49ff6c70-578b-4c50-8300-e71ba9d63987)



ii) Using Laplacian Operator:

![image](https://github.com/Jayakrishnan22003251/IMPLEMENTATION-OF-FILTERSS/assets/120232371/b82857c3-6691-466e-951c-f1063731e78c)



## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
