# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Read and show the image
### Step2
Apply the filtering technique that we want to perform
### Step3
Show the filtered image

## Program:
### Developed By   : ANU VARSHINI M B
### Register Number: 212223240010
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
kernel1 = np.ones((11,11),np.float32)/121
box_filter = cv2.filter2D(original_image,-1,kernel1)
cv2.imshow('box_filter',box_filter)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
ii) Using Weighted Averaging Filter
```Python
#ii) Using Weighted Averaging Filter
import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weighted_filter = cv2.filter2D(original_image,-1,kernel2)
cv2.imshow('weighted_filter',weighted_filter)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
iii) Using Gaussian Filter
```Python
import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
gaussian_blur = cv2.GaussianBlur(src = original_image, ksize = (11,11), sigmaX=0,
sigmaY=0)
cv2.imshow('gaussian_filter',gaussian_blur)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
iv) Using Median Filter
```Python
#iv) Using Median Filter
import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
median = cv2.medianBlur(src=original_image,ksize = 11)
cv2.imshow('median_filter',median)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
#i) Using Laplacian Kernal
import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
cv2.imshow('laplacian_kernel',laplacian_kernel)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
ii) Using Laplacian Operator
```Python
import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
laplacian_operator = cv2.Laplacian(original_image,cv2.CV_64F)
cv2.imshow('laplacian_operator',laplacian_operator)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## OUTPUT:
### original image
![origi](https://github.com/JEEVAABI/IMPLEMENTATION-OF-FILTERSS/assets/93427098/6b6f4f09-8bae-4ef1-93a5-ee1da10d483f)
### 1. Smoothing Filters

i) Using Averaging Filter
![boxfil](https://github.com/JEEVAABI/IMPLEMENTATION-OF-FILTERSS/assets/93427098/8f969c65-4629-4957-98ed-cf08a1dea710)

ii) Using Weighted Averaging Filter
![weight](https://github.com/JEEVAABI/IMPLEMENTATION-OF-FILTERSS/assets/93427098/ccce2e3c-1dde-476e-9a7e-b4e306052810)

iii) Using Gaussian Filter
![gauss](https://github.com/JEEVAABI/IMPLEMENTATION-OF-FILTERSS/assets/93427098/069b5660-8536-4499-81ae-242970b0ed66)

iv) Using Median Filter
![median](https://github.com/JEEVAABI/IMPLEMENTATION-OF-FILTERSS/assets/93427098/7a79815a-4848-4f9a-92e4-28b3cd7ec281)

### 2. Sharpening Filters

i) Using Laplacian Kernal
![kernal](https://github.com/JEEVAABI/IMPLEMENTATION-OF-FILTERSS/assets/93427098/177f6248-52c5-4fe6-9665-dd3bdbbcd9a9)

ii) Using Laplacian Operator
![laplacian](https://github.com/JEEVAABI/IMPLEMENTATION-OF-FILTERSS/assets/93427098/151d4d05-514b-441b-9168-d2ac40fc29f0)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
