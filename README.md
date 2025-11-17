## Name: MOHAMMAD SHAHIL
## Reg: 212223240044
# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.


### Step2:
Create the Text using cv2.putText.


### Step3:
Create the structuring element.

### Step4:
Perform opening operation and display the result

### Step5:
Similarly, perform closing operation and display the result

 
## Program:

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'PRIYADHARSHINI P', (40, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')
# Closing is dilation followed by erosion
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.title("Closing Operation")
plt.axis('off')
```
## Output:

### Display the input Image
![WhatsApp Image 2025-11-17 at 09 17 49_2cb5b3cf](https://github.com/user-attachments/assets/abf6429b-76c9-4dd5-98a7-610dfca66a88)



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
