# IMPLEMENTATION-OF-FILTERSS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7
### Algorithm:
### Step1
Import cv2, matplotlib.py libraries and read the saved images using cv2.imread().

### Step2
Convert the saved BGR image to RGB using cvtColor().

### Step3
By using the following filters for image smoothing:filter2D(src, ddepth, kernel), Box filter,Weighted Average filter,GaussianBlur(src, ksize, sigmaX[, dst[, sigmaY[, borderType]]]), medianBlur(src, ksize),and for image sharpening:Laplacian Kernel,Laplacian Operator.

### Step4
Apply the filters using cv2.filter2D() for each respective filters.

### Step5
Plot the images of the original one and the filtered one using plt.figure() and cv2.imshow().

### Developed By   : PERARASU M
### Register Number: 212222100033

## Program:
### 1. Smoothing Filters
i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("pr.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(8,8))
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
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("pr.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weighted_filter = cv2.filter2D(original_image,-1,kernel2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(weighted_filter)
plt.title("Weighted Averaging Filter Image")
plt.axis("off")
```
iii) Using Gaussian Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("pr.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
gaussian_blur = cv2.GaussianBlur(src = original_image, ksize = (11,11), sigmaX=0, sigmaY=0)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Filter Image")
plt.axis("off")
```
iv) Using Median Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("pr.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
median = cv2.medianBlur(src=original_image,ksize = 11)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Filter Image")
plt.axis("off")
```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("pr.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_kernel)
plt.title("Laplacian kernelFiltered Image")
plt.axis("off")
```
ii) Using Laplacian Operator
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("pr.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
laplacian_operator = cv2.Laplacian(original_image,cv2.CV_64F)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_operator)
plt.title(" Laplacian operator Filtered Image")
plt.axis("off")
```
## OUTPUT:
### 1. Smoothing Filters
i) Using Averaging Filter

![image](https://github.com/PERARASU10/IMPLEMENTATION-OF-FILTERSS/assets/118348589/d96a70e3-d715-4af5-a415-80be973e8558)


ii) Using Weighted Averaging Filter

![image](https://github.com/PERARASU10/IMPLEMENTATION-OF-FILTERSS/assets/118348589/e292c384-462b-4a2f-8b8b-a6e8ec8922f2)


iii) Using Gaussian Filter

![image](https://github.com/PERARASU10/IMPLEMENTATION-OF-FILTERSS/assets/118348589/c140e8c8-d63f-4c62-b972-62d07e6988f7)


iv) Using Median Filter

![image](https://github.com/PERARASU10/IMPLEMENTATION-OF-FILTERSS/assets/118348589/9b5cfecf-4f56-4132-8dfd-889f2da9d9c2)


### 2. Sharpening Filters

i) Using Laplacian Kernal

![image](https://github.com/PERARASU10/IMPLEMENTATION-OF-FILTERSS/assets/118348589/5b4c1ecf-317e-4f2b-8a65-d866611a65ff)


ii) Using Laplacian Operator

![image](https://github.com/PERARASU10/IMPLEMENTATION-OF-FILTERSS/assets/118348589/19c115a0-6cba-4940-94cf-ae2757a9f046)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
