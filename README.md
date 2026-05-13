# HOUGH-TRANSFORM

## Aim:
To write a Python program to detect the lines using Hough Transform.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import all the necessary modules for the program.
### Step2:

Load a image using imread() from cv2 module.
### Step3:

Convert the image to grayscale.
### Step4:

Using Canny operator from cv2,detect the edges of the image.
### Step5:

Using the HoughLinesP(),detect line co-ordinates for every points in the images.Using For loop,draw the lines on the found co-ordinates.Display the image.

## Program:
```
NAME:VEDHANTH H
REG NO: 212224240181
```
### Input Image:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('Qn_7_.jpg')  
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Input Image")
plt.axis('off')
```
## Grayscale Image:
```
plt.imshow(gray_image, cmap='gray')
plt.title("Grayscale Image")
plt.axis('off')
```
## Canny Edge Detector:
```
edges = cv2.Canny(gray_image, 50, 150)  
plt.imshow(edges, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis('off')
```
## Result of Hough Transform:
```
lines = cv2.HoughLinesP(edges, 1, np.pi / 180, 100, minLineLength=50, maxLineGap=10)
for line in lines:
    x1, y1, x2, y2 = line[0]  
    cv2.line(image, (x1, y1), (x2, y2), (0, 255, 0), 2)  
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB)) 
plt.title("Result of Hough Transform")
plt.axis('off') 
```
## Output

### Input image 
<img width="515" height="390" alt="image" src="https://github.com/user-attachments/assets/086158a8-8171-4757-bb24-15e68340055f" />


### grayscale image
<img width="515" height="390" alt="image" src="https://github.com/user-attachments/assets/d586053f-69d6-4df0-8bb9-f761f5982d64" />


### Canny Edge detector output
<img width="515" height="390" alt="image" src="https://github.com/user-attachments/assets/38f9c9b0-889b-4d00-abc4-45b9f3ee264e" />


### Display the result of Hough transform
<img width="515" height="390" alt="image" src="https://github.com/user-attachments/assets/19b0cb1b-7701-4a0b-be9b-4c4733bfda48" />



## Result:
Thus, the image has been successfully converted.
