# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

## Step 1:
Import the necessary packages.

## Step 2:
Create the Text using cv2.putText

## Step 3:
Create the structuring element.

## Step 4:
Use Opening operation.

## Step 5:
Use Closing Operatio
 
## Program:

```
/*
Developed by   : M.GUNASEKHAR
Register Number: 212221240014
*/
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'guna',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()

# Create the structuring element 

kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation

image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()

# Use Closing Operation

image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()




```
## Output:

### Display the input Image

![OUTPUT](?raw=true)

### Display the result of Opening

![OUTPUT](?raw=true)

### Display the result of Closing

![OUTPUT](?raw=true)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
