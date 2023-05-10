# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.


### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.

 
## Program:

``` Python
Developed by : PAVAN MUDI
Register Number: 212220230067
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'PAVAN MUDI',(5,70),font,2,(255),5,cv2.LINE_AA)
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
![DIP P11-1](https://github.com/mudipavan/Opening-and-Closing/assets/94828517/a970702c-7d77-450c-83d4-27068ce55e90)


### Display the result of Opening
![DIP P11-2](https://github.com/mudipavan/Opening-and-Closing/assets/94828517/e7dbc018-b6b2-4fe1-9be4-a6b8424a21ea)


### Display the result of Closing
![DIP P11-3](https://github.com/mudipavan/Opening-and-Closing/assets/94828517/8c16855b-5837-44d9-8242-0cc435d27375)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
