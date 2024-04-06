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
### Developed By   :Subhikshaa  
### Register Number:212222230151
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

### Original image 
![image](https://github.com/Subhikshaa13/Implementation-of-filter/assets/118787344/4a7a5979-7ceb-4160-a88f-01fb0ee4f974)

### 1. Smoothing Filters




i) Using Averaging Filter

![image](https://github.com/Subhikshaa13/Implementation-of-filter/assets/118787344/2426d47d-0c9b-47a9-893f-4b3fce8ef9af)


ii) Using Weighted Averaging Filter
![image](https://github.com/Subhikshaa13/Implementation-of-filter/assets/118787344/62002fea-9e96-4ddd-b3a3-30d04d989a4e)


iii) Using Gaussian Filter
![image](https://github.com/Subhikshaa13/Implementation-of-filter/assets/118787344/2b8e84a3-c0b1-49ef-ada8-e41ae03a20a4)


iv) Using Median Filter
![image](https://github.com/Subhikshaa13/Implementation-of-filter/assets/118787344/fcdfc634-2b0a-46e2-a1ea-ccb889afdece)


### 2. Sharpening Filters


i) Using Laplacian Kernal
![image](https://github.com/Subhikshaa13/Implementation-of-filter/assets/118787344/57c6dc4b-707d-4eb5-bd3b-a7f20ec58863)


ii) Using Laplacian Operator
![image](https://github.com/Subhikshaa13/Implementation-of-filter/assets/118787344/b1722077-da98-4131-a2a8-c3c94842a053)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
