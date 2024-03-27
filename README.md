# Histogram-of-an-images
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
```python
# Developed By: Kamali E
# Register Number: 212222110015






```
## Output:
### Input Grayscale Image and Color Image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("i1")
color_image = cv2.imread("i3",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Histogram of Grayscale Image and any channel of Color Image
```
import numpy as np
import cv2
Gray_image = cv2.imread("i1")
Color_image = cv2.imread("i3")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```

## Histogram Equalization of Grayscale Image
```
import cv2
gray_image = cv2.imread("i1",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Input Grayscale Image and Color Image

![316282552-781fbb71-918f-4832-853c-4d28ad447338](https://github.com/Kamali22004796/Histogram-of-an-images/assets/120567837/8c5b4af0-3810-45a3-97f6-9455da89c45d)


![316282563-78807470-39ea-4f86-b626-b855fc1530d9](https://github.com/Kamali22004796/Histogram-of-an-images/assets/120567837/3eabf6ca-ac20-418e-8644-ccb46b69db4c)

### Histogram of Grayscale Image and any channel of Color Image


![316282600-0402280b-e34f-481b-a411-d3ebdc014b0d](https://github.com/Kamali22004796/Histogram-of-an-images/assets/120567837/ea1db867-e3a3-4a7e-b4b0-b4187551beda)


![316282613-191898b1-afd0-47b2-b259-e56ed477e37b](https://github.com/Kamali22004796/Histogram-of-an-images/assets/120567837/e2dd406f-1c10-4b12-aaf5-72ff31d0e655)


![316282625-4403ca4c-ff02-464e-98ec-d1602d06ffc4](https://github.com/Kamali22004796/Histogram-of-an-images/assets/120567837/bd6a8d6d-785b-4d8f-b5e2-d514404860dc)


![316282630-46e59035-511a-44b4-b13e-d06f294e5126](https://github.com/Kamali22004796/Histogram-of-an-images/assets/120567837/ac0006a9-4f3d-4da6-bdd9-b049c17f1abe)


## Histogram Equalization of Grayscale Image

![316282675-ee3b9a46-65ab-4266-94f9-66f8cd7b5241](https://github.com/Kamali22004796/Histogram-of-an-images/assets/120567837/9929bbb5-6e33-4ae4-8076-9ec65b07616d)


![316282894-99907d7a-121b-4775-8adb-e454c723d429](https://github.com/Kamali22004796/Histogram-of-an-images/assets/120567837/de7df268-042b-403c-947d-990dc6c8781c)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
