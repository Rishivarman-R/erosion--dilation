# Implementation-of-Erosion-and-Dilation
## Name: Rishivarman R
## Reg No.: 212224100050
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
Dilate  the image
 
## Program:

```
!pip install opencv-python -q

import cv2
import numpy as np
from matplotlib import pyplot as plt

img1 = np.zeros((100, 500), dtype='uint8')


font = cv2.FONT_HERSHEY_COMPLEX_SMALL
cv2.putText(img1, 'Rishivarman R', (5, 70), font, 4, (255), 2, cv2.LINE_AA)

kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS, (5, 5))


img_dilate = cv2.dilate(img1, kernel1)
img_erode = cv2.erode(img1, kernel1)


plt.figure(figsize=(10, 3))

plt.subplot(1, 3, 1)
plt.imshow(img1, cmap='gray')
plt.title('Original')
plt.axis('off')

plt.subplot(1, 3, 2)
plt.imshow(img_dilate, cmap='gray')
plt.title('Dilated')
plt.axis('off')

plt.subplot(1, 3, 3)
plt.imshow(img_erode, cmap='gray')
plt.title('Eroded')
plt.axis('off')

plt.tight_layout()
plt.show()

```
## Output:
<img width="1409" height="157" alt="Screenshot 2025-11-12 140431" src="https://github.com/user-attachments/assets/830324c4-252d-4656-aaf9-c356cc482424" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
