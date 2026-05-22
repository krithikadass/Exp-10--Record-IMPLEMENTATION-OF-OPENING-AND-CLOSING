# Exp-10--Record-IMPLEMENTATION-OF-OPENING-AND-CLOSING
# OPENING--AND-CLOSING
# Name : Krithika Lakshmi M
# Reg No : 212224230134
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation
 
## Program:

```

import cv2
import numpy as np
import matplotlib.pyplot as plt

image = np.zeros((500, 500, 3), dtype=np.uint8)

font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Open and Close', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

kernel = np.ones((3, 3), np.uint8)

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Input Image with Text")
plt.axis('off')

opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  
plt.title("Opening Operation")
plt.axis('off')

plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))
plt.title("Closing Operation")
plt.axis('off')



```
## Output:

### Display the input Image

<img width="693" height="560" alt="image" src="https://github.com/user-attachments/assets/c7f96df0-12de-4288-ae6b-059f68456bae" />



### Display the result of Opening

<img width="690" height="565" alt="image" src="https://github.com/user-attachments/assets/4783b490-c279-43f5-aa9d-5001ede13a9f" />


### Display the result of Closing

<img width="656" height="421" alt="image" src="https://github.com/user-attachments/assets/82250ac2-4c08-4e63-abcc-1ee9c96835f4" />



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
