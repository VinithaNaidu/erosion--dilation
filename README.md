# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages
### Step2:
Create the text using cv2.putText
### Step3:
Create the structuring element
### Step4:
Erode the image
### Step5:
Dilate the Image
## Program:
``` Python
Developed by : D.Vinitha
Register Number : 212222230175
```
# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'B M W',(80,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
# Create the structuring element
```python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
# Erode the image
```python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
# Dilate the image
```python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image
![image](https://github.com/Nagul71/erosion--dilation/assets/118661118/ed4d03f3-0b49-4fbc-98e9-d8b06c2a15a2)


### Display the Eroded Image
![image](https://github.com/Nagul71/erosion--dilation/assets/118661118/464c52fb-70bc-452e-a43e-ffcc9d9981ca)


### Display the Dilated Image
![image](https://github.com/Nagul71/erosion--dilation/assets/118661118/f67c4477-1e87-4a6e-acbf-8b9f1f3f5ad1)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
