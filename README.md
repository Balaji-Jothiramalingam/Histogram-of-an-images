## Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Read the gray and color image using imread()

## Step2:
Print the image using imshow().

## Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

## step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

## Step5:
The Histogram of gray scale image and color image is shown.

## Program:
# Developed By: BALAJI J
# Register Number: 212221243001

## Input Grayscale Image and Color Image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('gray.jpg')
color_image = cv2.imread('color.jpg')
cv2.imshow("Gray image",gray_image)
cv2.imshow("color image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Histogram of Grayscale Image
```
import numpy as np
gray_image=cv2.imread('gray.jpg')
import matplotlib.pyplot as plt 
gray_hist=cv2.calcHist(gray_image,[0],None,[255],[0,255])
plt.figure(figsize=(10,6))
plt.subplot(1,2,1)
plt.imshow(gray_image)
plt.subplot(1,2,2)
plt.title("Histogram")
plt.xlabel("Grayscale value")
plt.ylabel("pixel count")
plt.stem(gray_hist)
plt.show()
```
## Histogram of any channel of Color Image
```
import numpy as np
color_image=cv2.imread('color.jpg')
color_img=cv2.cvtColor(color_image,cv2.COLOR_BGR2RGB)
import matplotlib.pyplot as plt 
color_hist=cv2.calcHist(color_img,[0],None,[255],[0,255])
plt.figure(figsize=(8,4))
plt.subplot(1,2,1)
plt.imshow(color_img)
plt.subplot(1,2,2)
plt.title("Histogram")
plt.xlabel("Colorscale value")
plt.ylabel("pixel count")
plt.stem(color_hist)
plt.show()
```
## Histogram Equalization of Grayscale Image
```
import cv2
gray_image = cv2.imread("gray.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
## Input Grayscale Image and Color Image

![image](https://github.com/user-attachments/assets/06301631-f1e2-483a-9205-cf8d01e9fdd4)

## Histogram of Grayscale Image
![image](https://github.com/user-attachments/assets/f120281b-e150-4497-bc56-1ef0476bd8d2)


## Histogram of any channel of Color Image
![image](https://github.com/user-attachments/assets/364149b4-9737-4f1d-bf2f-1bb472053846)

## Histogram Equalization of Grayscale Image.
![image](https://github.com/user-attachments/assets/6efdfc9c-dcba-4ffb-bb1a-5fd3cbe34c56)


## Result:
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
