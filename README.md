
# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.
## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1
</br>
Import the required libraries.
</br> 

### Step2
</br>
Convert the image from BGR to RGB.
</br> 

### Step3
</br>
Apply the required filters for the image separately.
</br> 

### Step4
</br>
Plot the original and filtered image by using matplotlib.pyplot.
</br> 

### Step5
</br>
End the program.
</br> 

## Program
### Developed By   : NISHA D
### Register Number: 212223230143
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("/content/thala.png")
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
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv)Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.title("Median Blur")
plt.axis('off')
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator
```
median=cv2.medianBlur(image2,13)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters
</br>

# i) Using Averaging Filter
![image](https://github.com/user-attachments/assets/083ff4f6-d113-4bb9-a568-b5cc783b6626)


# ii)Using Weighted Averaging Filter
![image](https://github.com/user-attachments/assets/2c79041b-0cb7-45ee-b440-d8fef69cef08)


# iii)Using Gaussian Filter
![image](https://github.com/user-attachments/assets/ef6cb695-db3e-4105-96d8-d6c672f085ea)


# iv) Using Median Filter
!![image](https://github.com/user-attachments/assets/95975fb2-1cfd-4424-9377-daa9efc96e93)


### 2. Sharpening Filters


# i) Using Laplacian Kernal
![image](https://github.com/user-attachments/assets/65f0a545-69eb-476a-9612-8e4633a2587b)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
