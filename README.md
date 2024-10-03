
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
# Developed By: BALAJI J
# Register Number: 212221243001

```
import cv2
import numpy as np
from matplotlib import pyplot as plt

image = cv2.imread('seed.jpg')
                   
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

equalized_image = cv2.equalizeHist(gray_image)

plt.figure(figsize=(10, 7))

plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

plt.subplot(2, 2, 3)
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

plt.subplot(2, 2, 4)
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

plt.tight_layout()
plt.show()
```
## Output:
### Input Grayscale Image and Col

![325460458-5fa788f0-f9d2-4cab-a9e2-3987cb3f7c5c](https://github.com/user-attachments/assets/01619dc4-f11e-4963-bbcc-ad5e2d1e57e2)
or Image


### Histogram of Grayscale Image and any channel of Color Image

![325461226-b7e9e2ba-38a0-483e-8dff-1a40a536579a](https://github.com/user-attachments/assets/f30357ab-76c9-482a-821c-5f3e6b96a3d6)

![325461316-20275cd9-82f0-4f2d-b500-721171473754](https://github.com/user-attachments/assets/9e05f840-aa31-43f7-a395-1f981c2fd120)


### Histogram Equalization of Grayscale Image.


![325461911-ae2dae77-5fd4-458c-b101-281c8d324405](https://github.com/user-attachments/assets/e66715ce-28be-4651-ad90-3e14272c326b)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
