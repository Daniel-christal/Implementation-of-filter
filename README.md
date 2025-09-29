# Implementation-of-filter:
# Developed By:Daniel C
# Reg no:212223240023
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
### Developed By   :Daniel C
### Register Number:212223240023
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("cad.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
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
plt.show()




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
iv)Using Median Filter
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
i) Using Laplacian Linear Kernal
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
</br>

i) Using Averaging Filter
<img width="850" height="277" alt="image" src="https://github.com/user-attachments/assets/c2c73a83-a73b-420f-b4a1-ac3387125a7f" />


ii)Using Weighted Averaging Filter
<img width="847" height="272" alt="image" src="https://github.com/user-attachments/assets/27c0da9a-845e-4f9d-bbf0-818bba1fd786" />


iii)Using Gaussian Filter
<img width="850" height="288" alt="image" src="https://github.com/user-attachments/assets/9cd5c24c-f38c-47db-ac57-1e2366618152" />


iv) Using Median Filter
<img width="857" height="276" alt="image" src="https://github.com/user-attachments/assets/d3909570-16a2-40e7-8a96-00e8f308d9ec" />


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
<img width="850" height="283" alt="image" src="https://github.com/user-attachments/assets/a7d0fc4c-f733-4f27-9900-348532bbbf6f" />


ii) Using Laplacian Operator
<img width="860" height="277" alt="image" src="https://github.com/user-attachments/assets/5717c20c-e4b2-4538-9bdb-2f4dcde28357" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
