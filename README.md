# EX-10--Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Import the necessary packages.

### Step2:

Create the text image using cv2.putText().

### Step3:

Create the structuring kernel for image dilation and erosion.

### Step4:

Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:

Plot the images using plt.imshow().

 
## Program:
```Python
Developed By: Gunaseelan G
Register  No: 212221230031
```

``` Python
# Import the necessary packages

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Create the Text using cv2.putText

# Create the text using cv2.putText
text_image = np.zeros((100,190),dtype = 'uint8')
font = cv2.FONT_HERSHEY_COMPLEX_SMALL
cv2.putText(text_image,"Guna",(5,70),font,2,(255),2,cv2.LINE_AA) 
plt.title("Original Image")
plt.imshow(text_image,'bone')
plt.axis('off')

# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(4,4))


# Erode the image

image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'bone')
plt.axis('off')


# Dilate the image

image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'bone')
plt.axis('off')



```
## Output:

### Display the input Image
![out1](https://github.com/Guru-Guna/Implementation-of-Erosion-and-Dilation/assets/93427255/fd371568-463a-4f82-8c64-3db79ee592c6)



### Display the Eroded Image
![out2](https://github.com/Guru-Guna/Implementation-of-Erosion-and-Dilation/assets/93427255/10c1fbc7-e81c-432d-9827-b2a151933046)



### Display the Dilated Image
![out3](https://github.com/Guru-Guna/Implementation-of-Erosion-and-Dilation/assets/93427255/deb38200-7c37-4936-a63a-096d256e6831)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
